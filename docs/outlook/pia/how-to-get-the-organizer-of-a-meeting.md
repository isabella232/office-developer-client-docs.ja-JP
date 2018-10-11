---
title: 会議の開催者を取得する
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 87d8486b29039f87cb0cbedd2693ce1b4d38b1dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406772"
---
# <a name="get-the-organizer-of-a-meeting"></a><span data-ttu-id="0fb12-102">会議の開催者を取得する</span><span class="sxs-lookup"><span data-stu-id="0fb12-102">Get the organizer of a meeting</span></span>

<span data-ttu-id="0fb12-103">この例では、プログラムによって会議の開催者を返す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0fb12-103">This example shows how to programmatically return the organizer of a meeting.</span></span>

## <a name="example"></a><span data-ttu-id="0fb12-104">例</span><span class="sxs-lookup"><span data-stu-id="0fb12-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0fb12-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="0fb12-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="0fb12-106">次のコード サンプルの GetMeetingOrganizer では、会議を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) 型のパラメーターを受け取り、[PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトと [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) メソッドを使用して、**AppointmentItem** オブジェクトの [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) を取得します。</span><span class="sxs-lookup"><span data-stu-id="0fb12-106">In the following code example,   takes a parameter of type AppointmentItem that represents a meeting, and uses the PropertyAccessor object and the GetProperty(String) method to obtain the EntryID for the AppointmentItem object.</span></span> <span data-ttu-id="0fb12-107">**EntryID** を取得した後、[GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) メソッドを使用して、会議の開催者を表す [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="0fb12-107">Once the **EntryID** is obtained, the example uses the [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) method to return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object that represents the organizer of the meeting.</span></span>

<span data-ttu-id="0fb12-108">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0fb12-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="0fb12-109">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fb12-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="0fb12-110">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0fb12-110">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Outlook.AddressEntry GetMeetingOrganizer(Outlook.AppointmentItem appt)
{
    if (appt == null)
    {
        throw new ArgumentNullException();
    }
    string PR_SENT_REPRESENTING_ENTRYID =
        @"https://schemas.microsoft.com/mapi/proptag/0x00410102";
    string organizerEntryID =
        appt.PropertyAccessor.BinaryToString(
            appt.PropertyAccessor.GetProperty(
            PR_SENT_REPRESENTING_ENTRYID));
    Outlook.AddressEntry organizer =
        Application.Session.
        GetAddressEntryFromID(organizerEntryID);
    if (organizer != null)
    {
        return organizer; 
    }
    else
    {
        return null;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0fb12-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="0fb12-111">See also</span></span>

- [<span data-ttu-id="0fb12-112">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="0fb12-112">Meeting Requests</span></span>](meeting-requests.md)

