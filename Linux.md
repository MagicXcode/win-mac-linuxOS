1. 多行命令写到一行 ：`;`间隔。只有执行了前一个才会执行后一个

2. 添加当前路径到系统路径: 

   要将当前路径添加到Linux系统的环境变量中，可以使用以下两种方法：命令行方式和编辑配置文件方式（使用vim编辑器）。

   1. 命令行方式：
      打开终端并输入以下命令：
      ```
      export PATH=$PATH:$(pwd)
      ```
      这将把当前路径添加到系统的环境变量`PATH`中。这种方式仅在当前终端会话中有效，如果要在每次登录时都自动生效，可以将该命令添加到`~/.bashrc`文件（对于bash shell）或`~/.bash_profile`文件（对于bash shell和登录shell）中。

   2. 编辑配置文件方式（使用vim编辑器）：
      使用vim编辑器打开相应的配置文件，并添加一行将当前路径添加到环境变量的代码。

      - 对于bash shell，可以使用以下命令打开`~/.bashrc`文件：
        ```
        vim ~/.bashrc
        ```

      - 对于bash shell和登录shell，可以使用以下命令打开`~/.bash_profile`文件：
        ```
        vim ~/.bash_profile
        ```

      在文件的末尾或合适的位置添加以下代码：
      ```
      export PATH=$PATH:$(pwd)
      ```

      保存并关闭文件。然后，在新的终端会话中，该配置将自动加载。

   请注意，使用vim编辑器进行文件编辑需要一些基本的vim操作知识。如果您对vim不熟悉，可以使用其他文本编辑器（如nano）来编辑文件。

   无论使用哪种方法，确保小心编辑文件并正确保存更改。修改环境变量可能会对系统产生影响，因此请谨慎操作。

   希望这些信息对您有所帮助。如有进一步问题，请随时提问。

3. 要将当前路径添加到Linux系统的环境变量中，您可以使用`echo`命令和重定向操作来实现。

   1. 打开终端并输入以下命令：
      ```
      echo 'export PATH=$PATH:'$(pwd) >> ~/.bashrc
      ```
      这将使用`echo`命令和重定向操作将一条命令追加到`~/.bashrc`文件的末尾。该命令将当前路径添加到系统的环境变量`PATH`中。

      注意，`~/.bashrc`文件是bash shell的启动脚本文件，它在每次打开新终端时都会被执行。

   2. 保存并关闭终端。

   3. 在新的终端会话中，环境变量将自动加载，并且当前路径已添加到`PATH`中。

   请注意，使用`echo`命令和重定向操作修改配置文件时要小心。确保正确地追加命令到文件末尾，并避免破坏其他配置。

   希望这能帮助您将当前路径添加到系统的环境变量中。如有进一步问题，请随时提问。