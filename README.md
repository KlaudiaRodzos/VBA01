# VBA01
Function MojaFunkcja()
MojaFunkcja = "To jest wynik funkcji"
End Function

Sub FunExample()
 
Dim intValue As Integer
intValue = InputBox("Wprowadź wartość")
MsgBox (Sqr(intValue))
 
End Sub

Public Sub CreateTable(ByVal firstColumnHeader As String, _
    ByVal secondColumnHeader As String)

    Me.Paragraphs(1).Range.InsertParagraphBefore()
    Dim table1 As Word.Table = Me.Tables.Add(Me.Paragraphs(1).Range, 2, 2)

    With table1
        .Style = "Table Professional"
        .Cell(1, 1).Range.Text = firstColumnHeader
        .Cell(1, 2).Range.Text = secondColumnHeader
    End With
End Sub
