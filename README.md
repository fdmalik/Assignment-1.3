# Assignment-1.3

        Dim mName As String = ""
        Dim mId As Integer = 0
        Dim found As Boolean = False
        Dim SearchFor As String

        Console.Write("Please type the Name of the member you would like to search for : ")
        SearchFor = Console.ReadLine

        FileOpen(1, "c:\Assignment 1\mRec.txt", OpenMode.Input)

        While Not EOF(1) And found = False

            Input(1, mName)
            Input(1, mId)

            If LCase(mName) = LCase(SearchFor) Then
                found = True

                Console.WriteLine(" Member Name : " & mName)
                Console.WriteLine("Member I.D : " & mId)


            End If
        End While
        FileClose(1)

        If found = False Then Console.WriteLine("Sorry, the Name of the member you are looking for matches no one in our records!")

        Console.ReadKey()
