WPF实现半透明背景的弹框
https://blog.csdn.net/u011389297/article/details/52203242

[C# Net]GraphicsでPictureBoxを透過させ、背景に図形を重ねて書く
https://kajindowsxp.com/net-graphics-overlay/

Transparent background on picturebox
https://www.codeproject.com/questions/157092/transparent-background-on-picturebox

C#实现winform仿div+css半透明遮罩效果
https://www.programminghunter.com/article/2764782829/

C#實現Winform自定義半透明遮罩層
https://www.twblogs.net/a/5b7e58952b7177683856c8ff


<Runtime.InteropServices.DllImport("USER32.DLL", CharSet:=Runtime.InteropServices.CharSet.Unicode)>
Public Shared Function FindWindow(lpClassName As String, lpWindowName As String) As IntPtr : End Function

<Runtime.InteropServices.DllImport("USER32.DLL")>
Public Shared Function SetForegroundWindow(hWnd As IntPtr) As Boolean : End Function

Private Sub Button1_Click(sender As Object, e As EventArgs)
    Dim hCalcWindow As IntPtr = FindWindow(Nothing, "Calculator")

    If SetForegroundWindow(hCalcWindow) Then
        SendKeys.Send("10{+}10=")
    End If
End Sub

KB4564002
