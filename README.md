# Age-Calculator

Public Class AgeCalculator

Private Sub AgeCalculator_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

        Dim todaysDate As Date = Today

        Label2.Text = todaysDate.ToLongDateString

    End Sub

    Private Sub exitButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles exitButton.Click

        'CLOSE PROJECT.

        Me.Close()

    End Sub

    Private Sub clearButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles clearButton.Click

        'CLEAR CONTENTS.

        currentyearTextBox.Text = Nothing

        yearofbirthTextBox.Text = Nothing

        calculateLabel.Text = "Age"

    End Sub

    Private Sub calculateageButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles calculateageButton.Click

        Dim YEAR As Integer

        Dim YEAROFBIRTH As Integer

        Dim CALCULATion As Integer


        YEAR = Integer.Parse(currentyearTextBox.Text)

        YEAROFBIRTH = Integer.Parse(yearofbirthTextBox.Text)

        CALCULATion = (Integer.Parse(currentyearTextBox.Text) - Integer.Parse(yearofbirthTextBox.Text))

        With Me

            calculateLabel.Text = CALCULATion.ToString

        End With

    End Sub

End Class

