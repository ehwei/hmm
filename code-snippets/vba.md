# VBA

#### Convert all tables to text

```text
Sub Demo()
With ActiveDocument
  While .Tables.Count > 0
    With .Tables(1)
      With .Range.Font
        .Size = 8
        .ColorIndex = wdRed
      End With
      .ConvertToText Separator:=vbTab, NestedTables:=True
    End With
  Wend
End With
End Sub
```

source: [https://answers.microsoft.com/en-us/msoffice/forum/all/macro-to-find-all-tables-and-convert-them-into/c39b362f-43b4-4968-8208-29ea7c1d8af9](https://answers.microsoft.com/en-us/msoffice/forum/all/macro-to-find-all-tables-and-convert-them-into/c39b362f-43b4-4968-8208-29ea7c1d8af9)

