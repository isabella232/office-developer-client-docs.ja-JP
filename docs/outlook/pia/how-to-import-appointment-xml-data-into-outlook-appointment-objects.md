---
title: 予定の XML データを Outlook の予定オブジェクトにインポートする
TOCTitle: Import appointment XML data into Outlook appointment objects
ms:assetid: 166a648a-1c48-4984-8889-a7614cc277b1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462092(v=office.15)
ms:contentKeyID: 55119821
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fef3e924ed5f81d5d64e5ca77bc417c000866ad2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560509"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a>予定の XML データを Outlook の予定オブジェクトにインポートする

ここでは、XML 形式の予定データを読み取る方法、Outlook の [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトの既定の予定表にデータを保存する方法、および配列で予定オブジェクトを返す方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、Helmut Obertanner 氏が提供したものです。 Helmut 氏の得意分野は、Office Developer Tools for Visual Studio と Outlook です。 


次のコード例には、Sample クラスの CreateAppointmentsFromXml メソッドが含まれています。このメソッドは、Outlook アドイン プロジェクトの一部として実装されています。 それぞれのプロジェクトでは、[Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) 名前空間に基づいた、Outlook プライマリ互換運用機能アセンブリへの参照を追加しています。

CreateAppointmentsFromXml メソッドは、次の 2 つの入力パラメーターを受け取ります。

  - application は、信頼された Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクトです。

  - xml は、XML 文字列、または妥当な XML ファイルのパスを表す文字列のどちらかです。次のコード例では、以下の XML タグを使用して XML の予定データを区切っています。
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>予定データ</p></th>
    <th><p>区切りの XML タグ</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>予定データのセット全体</p></td>
    <td><p>appointments</p></td>
    </tr>
    <tr class="even">
    <td><p>セット内のそれぞれの予定</p></td>
    <td><p>appointment</p></td>
    </tr>
    <tr class="odd">
    <td><p>予定の開始時刻</p></td>
    <td><p>starttime</p></td>
    </tr>
    <tr class="even">
    <td><p>予定の終了時刻</p></td>
    <td><p>endtime</p></td>
    </tr>
    <tr class="odd">
    <td><p>予定の件名</p></td>
    <td><p>subject</p></td>
    </tr>
    <tr class="even">
    <td><p>予定の場所</p></td>
    <td><p>location</p></td>
    </tr>
    <tr class="odd">
    <td><p>予定の詳細</p></td>
    <td><p>body</p></td>
    </tr>
    </tbody>
    </table>


次の例は、*xml* パラメーターの入力データを示しています。

```xml
<?xml version="1.0" encoding="utf-8" ?> 
<appointments>
    <appointment>
        <starttime>2009-06-01T15:00:00</starttime>
        <endtime>2009-06-01T16:15:00</endtime>
        <subject>This is a Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T17:15:00</endtime>
        <subject>This is a second Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T18:15:00</endtime>
        <subject>This is a third Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
</appointments>
```

CreateAppointmentsFromXml メソッドは、Microsoft COM 実装の XML ドキュメント オブジェクト モデル (DOM) を使用して、xml が示す XML データの読み込みと処理を行います。CreateAppointmentsFromXml はまず、xml が示すのが XML データの有効なソースかどうかをチェックします。有効な場合は、XML ドキュメント [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)) にデータを読み込みます。有効でない場合は、CreateAppointmentsFromXml は例外をスローします。XML DOM の詳細については、「[DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\))」を参照してください。

CreateAppointmentsFromXml では、XML データ内の appointment タグで区切られた予定の子ノードごとに固有のタグを検索し、DOM を使用してデータを抽出して、そのデータを対応する **AppointmentItem** オブジェクトのプロパティ ([Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\))、[End](https://msdn.microsoft.com/library/bb623715\(v=office.15\))、[Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\))、[Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\))、および [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\))) に割り当てます。 その後、CreateAppointmentsFromXml では既定の予定表に予定を保存します。

CreateAppointmentsFromXml は[](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2)[、System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2)名前空間の[List \<T\> ](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2)クラスの Add メソッドを使用して、これらの AppointmentItem オブジェクトを集約します。 このメソッドは、XML データに含まれるすべての予定を処理すると、配列で AppointmentItem オブジェクトを返します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

次に、Visual Basic のコード例を示します。その後に、C\# のコード例を示します。



```vb
Imports System.IO
Imports System.Xml
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Function CreateAppointmentsFromXml(ByVal application As Outlook.Application, _
            ByVal xml As String) As Outlook.AppointmentItem()

            Dim appointments As New List(Of Outlook.AppointmentItem)
            Dim xmlDoc As New XmlDocument()

            ' If xml is an XML string, create the XML document directly.
            If xml.StartsWith("<?xml") Then
                xmlDoc.LoadXml(xml)
            ElseIf (File.Exists(xml)) Then
                xmlDoc.Load(xml)
            Else
                Throw New Exception("The input string is not valid XML data or the specified file doesn't exist.")
            End If


            ' Select all appointment nodes under the root appointments node.
            Dim appointmentNodes As XmlNodeList = xmlDoc.SelectNodes("appointments/appointment")

            For Each appointmentNode As XmlNode In appointmentNodes

                ' Create a new AppointmentItem object.
                Dim newAppointment As Outlook.AppointmentItem = _
                    DirectCast(application.CreateItem(Outlook.OlItemType.olAppointmentItem), _
                    Outlook.AppointmentItem)

                ' Loop over all child nodes, check the node name, and import the data into the appointment fields.

                For Each node As XmlNode In appointmentNode.ChildNodes
                    Select Case (node.Name)

                        Case "starttime"
                            newAppointment.Start = DateTime.Parse(node.InnerText)


                        Case "endtime"
                            newAppointment.End = DateTime.Parse(node.InnerText)


                        Case "subject"
                            newAppointment.Subject = node.InnerText


                        Case "location"
                            newAppointment.Location = node.InnerText


                        Case "body"
                            newAppointment.Body = node.InnerText


                    End Select
                Next

                ' Save the item in the default calendar.
                newAppointment.Save()
                appointments.Add(newAppointment)
            Next

            ' Return an array of new appointments.
            Return appointments.ToArray()
        End Function


    End Class
End Namespace
```



```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Text;
using System.Xml;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.AppointmentItem[] CreateAppointmentsFromXml(Outlook.Application application, 
            string xml)
        {
            // Create a list of appointment objects.
            List<Outlook.AppointmentItem> appointments = new 
                List<Microsoft.Office.Interop.Outlook.AppointmentItem>();
            XmlDocument xmlDoc = new XmlDocument();

            // If xml is an XML string, create the document directly. 
            if (xml.StartsWith("<?xml"))
            {
                xmlDoc.LoadXml(xml);
            }
            else if (File.Exists(xml))
            {
                xmlDoc.Load(xml);
            }
            else
            {
                throw new Exception(
                    "The input string is not valid XML data or the specified file doesn't exist.");
            }

            // Select all appointment nodes under the root appointments node.
            XmlNodeList appointmentNodes = xmlDoc.SelectNodes("appointments/appointment");
            foreach (XmlNode appointmentNode in appointmentNodes)
            {

                // Create a new AppointmentItem object.
                Outlook.AppointmentItem newAppointment = 
                    (Outlook.AppointmentItem)application.CreateItem(Outlook.OlItemType.olAppointmentItem);

                // Loop over all child nodes, check the node name, and import the data into the 
                // appointment fields.
                foreach (XmlNode node in appointmentNode.ChildNodes)
                {
                    switch (node.Name)
                    {

                        case "starttime":
                            newAppointment.Start = DateTime.Parse(node.InnerText);
                            break;

                        case "endtime":
                            newAppointment.End = DateTime.Parse(node.InnerText);
                            break;

                        case "subject":
                            newAppointment.Subject = node.InnerText;
                            break;

                        case "location":
                            newAppointment.Location = node.InnerText;
                            break;

                        case "body":
                            newAppointment.Body = node.InnerText;
                            break;

                    }
                }

                // Save the item in the default calendar.
                newAppointment.Save();
                appointments.Add(newAppointment);
            }

            // Return an array of new appointments.
            return appointments.ToArray();
        }

    }
}
```

## <a name="see-also"></a>関連項目

- [予定](appointments.md)

