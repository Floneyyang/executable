## No Subcommmands

This example demonstrates using Executable::Command to create a simple command line
interface without subcommands. (Note the Executable mixin could be used just
as well).

    class NoSubCommandCLI < Executable::Command

      attr :result

      def o?
        @o
      end

      def o=(flag)
        @o = flag
      end

      def call
        if o?
          @result = "with"
        else
          @result = "without"
        end
      end

    end

Execute the CLI on an example command line.

    cli = NoSubCommandCLI.run('')
    cli.result.assert == 'without'

Execute the CLI on an example command line.

    cli = NoSubCommandCLI.run('-o')
    cli.result.assert == 'with'

There are two important things to notices heres. Frist, that #main is being
called in each case. It is the method called with no other subcommands are
defined. And second, the fact the a `o?` method is defined to compliment the
`o=` writer, informs Executable that `-o` is an option _flag_, not taking
any parameters.

