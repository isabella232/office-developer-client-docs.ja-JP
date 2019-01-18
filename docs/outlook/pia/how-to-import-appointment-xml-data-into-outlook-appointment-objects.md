---
title: 予定の XML データを Outlook の予定オブジェクトにインポートする
TOCTitle: Import appointment XML data into Outlook appointment objects
ms:assetid: 166a648a-1c48-4984-8889-a7614cc277b1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462092(v=office.15)
ms:contentKeyID: 55119821
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0af86772fced3e69d1d28cf8d98a544e3b4d90d2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705387"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a><span data-ttu-id="2275c-102">予定の XML データを Outlook の予定オブジェクトにインポートする</span><span class="sxs-lookup"><span data-stu-id="2275c-102">Import appointment XML data into Outlook appointment objects</span></span>

<span data-ttu-id="2275c-103">ここでは、XML 形式の予定データを読み取る方法、Outlook の [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトの既定の予定表にデータを保存する方法、および配列で予定オブジェクトを返す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2275c-103">This topic shows how to read appointment data formatted in XML, save the data to Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) objects in the default calendar, and return the appointment objects in an array.</span></span>

## <a name="example"></a><span data-ttu-id="2275c-104">例</span><span class="sxs-lookup"><span data-stu-id="2275c-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2275c-105">次のコード例は、Helmut Obertanner 氏が提供したものです。</span><span class="sxs-lookup"><span data-stu-id="2275c-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="2275c-106">Helmut 氏の得意分野は、Office Developer Tools for Visual Studio と Outlook です。</span><span class="sxs-lookup"><span data-stu-id="2275c-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 


<span data-ttu-id="2275c-107">次のコード例には、Sample クラスの CreateAppointmentsFromXml メソッドが含まれています。このメソッドは、Outlook アドイン プロジェクトの一部として実装されています。</span><span class="sxs-lookup"><span data-stu-id="2275c-107">The following code examples contain the CreateAppointmentsFromXml method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="2275c-108">それぞれのプロジェクトでは、[Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) 名前空間に基づいた、Outlook プライマリ互換運用機能アセンブリへの参照を追加しています。</span><span class="sxs-lookup"><span data-stu-id="2275c-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="2275c-109">CreateAppointmentsFromXml メソッドは、次の 2 つの入力パラメーターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="2275c-109">The CreateAppointmentsFromXml method accepts two input parameters:</span></span>

  - <span data-ttu-id="2275c-110">application は、信頼された Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="2275c-110">application is a trusted Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

  - <span data-ttu-id="2275c-p103">xml は、XML 文字列、または妥当な XML ファイルのパスを表す文字列のどちらかです。次のコード例では、以下の XML タグを使用して XML の予定データを区切っています。</span><span class="sxs-lookup"><span data-stu-id="2275c-p103">xml is either an XML string, or a string that represents a path to a valid XML file. For the purpose of the following code examples, the XML delimits appointment data by using the following XML tags:</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="2275c-113">予定データ</span><span class="sxs-lookup"><span data-stu-id="2275c-113">Appointment data</span></span></p></th>
    <th><p><span data-ttu-id="2275c-114">区切りの XML タグ</span><span class="sxs-lookup"><span data-stu-id="2275c-114">Delimiting XML tag</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="2275c-115">予定データのセット全体</span><span class="sxs-lookup"><span data-stu-id="2275c-115">Entire set of appointment data</span></span></p></td>
    <td><p><span data-ttu-id="2275c-116">appointments</span><span class="sxs-lookup"><span data-stu-id="2275c-116">appointments</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="2275c-117">セット内のそれぞれの予定</span><span class="sxs-lookup"><span data-stu-id="2275c-117">Each appointment in the set</span></span></p></td>
    <td><p><span data-ttu-id="2275c-118">appointment</span><span class="sxs-lookup"><span data-stu-id="2275c-118">appointment</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="2275c-119">予定の開始時刻</span><span class="sxs-lookup"><span data-stu-id="2275c-119">Start time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="2275c-120">starttime</span><span class="sxs-lookup"><span data-stu-id="2275c-120">starttime</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="2275c-121">予定の終了時刻</span><span class="sxs-lookup"><span data-stu-id="2275c-121">End time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="2275c-122">endtime</span><span class="sxs-lookup"><span data-stu-id="2275c-122">endtime</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="2275c-123">予定の件名</span><span class="sxs-lookup"><span data-stu-id="2275c-123">Title of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="2275c-124">subject</span><span class="sxs-lookup"><span data-stu-id="2275c-124">subject</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="2275c-125">予定の場所</span><span class="sxs-lookup"><span data-stu-id="2275c-125">Location of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="2275c-126">location</span><span class="sxs-lookup"><span data-stu-id="2275c-126">location</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="2275c-127">予定の詳細</span><span class="sxs-lookup"><span data-stu-id="2275c-127">Details of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="2275c-128">body</span><span class="sxs-lookup"><span data-stu-id="2275c-128">body</span></span></p></td>
    </tr>
    </tbody>
    </table>


<span data-ttu-id="2275c-129">次の例は、*xml* パラメーターの入力データを示しています。</span><span class="sxs-lookup"><span data-stu-id="2275c-129">The following example shows input data for the *xml* parameter.</span></span>

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

<span data-ttu-id="2275c-p104">CreateAppointmentsFromXml メソッドは、Microsoft COM 実装の XML ドキュメント オブジェクト モデル (DOM) を使用して、xml が示す XML データの読み込みと処理を行います。CreateAppointmentsFromXml はまず、xml が示すのが XML データの有効なソースかどうかをチェックします。有効な場合は、XML ドキュメント [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)) にデータを読み込みます。有効でない場合は、CreateAppointmentsFromXml は例外をスローします。XML DOM の詳細については、「[DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2275c-p104">The CreateAppointmentsFromXml method uses the Microsoft COM implementation of the XML Document Object Model (DOM) to load and process the XML data that xml provides. CreateAppointmentsFromXml first checks whether xml specifies a valid source of XML data. If so, it loads the data into an XML document, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). Otherwise, CreateAppointmentsFromXml throws an exception. For more information about the XML DOM, see [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span></span>

<span data-ttu-id="2275c-135">CreateAppointmentsFromXml では、XML データ内の appointment タグで区切られた予定の子ノードごとに固有のタグを検索し、DOM を使用してデータを抽出して、そのデータを対応する **AppointmentItem** オブジェクトのプロパティ ([Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\))、[End](https://msdn.microsoft.com/library/bb623715\(v=office.15\))、[Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\))、[Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\))、および [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\))) に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2275c-135">For each appointment child node delimited by the appointment tag in the XML data, CreateAppointmentsFromXml looks for specific tags, uses the DOM to extract the data, and assigns the data to corresponding properties of an **AppointmentItem** object: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)), and [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span></span> <span data-ttu-id="2275c-136">その後、CreateAppointmentsFromXml では既定の予定表に予定を保存します。</span><span class="sxs-lookup"><span data-stu-id="2275c-136">CreateAppointmentsFromXml then saves the appointment to the default calendar.</span></span>

<span data-ttu-id="2275c-137">CreateAppointmentsFromXml では、[System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) 名前空間内の [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) クラスの [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) メソッドを使用して、該当する AppointmentItem オブジェクトを集約します。</span><span class="sxs-lookup"><span data-stu-id="2275c-137">CreateAppointmentsFromXml uses the [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) method of the [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) class in the [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) namespace to aggregate these AppointmentItem objects.</span></span> <span data-ttu-id="2275c-138">このメソッドは、XML データに含まれるすべての予定を処理すると、配列で AppointmentItem オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="2275c-138">When the method has processed all the appointments in the XML data, it returns the AppointmentItem objects in an array.</span></span>

<span data-ttu-id="2275c-139">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2275c-139">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="2275c-140">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2275c-140">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="2275c-141">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2275c-141">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="2275c-142">次に、Visual Basic のコード例を示します。その後に、C\# のコード例を示します。</span><span class="sxs-lookup"><span data-stu-id="2275c-142">The following is the Visual Basic code example, followed by the C\# code example.</span></span>



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

## <a name="see-also"></a><span data-ttu-id="2275c-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="2275c-143">See also</span></span>

- [<span data-ttu-id="2275c-144">予定</span><span class="sxs-lookup"><span data-stu-id="2275c-144">Appointments</span></span>](appointments.md)

