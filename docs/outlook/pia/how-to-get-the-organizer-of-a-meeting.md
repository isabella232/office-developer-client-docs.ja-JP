---
title: 会議の開催者を取得する
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 321cf15e0f1144518d526c3897863e9bf3d681dd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583150"
---
# <a name="get-the-organizer-of-a-meeting"></a>会議の開催者を取得する

この例では、プログラムによって会議の開催者を返す方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

次のコード サンプルの GetMeetingOrganizer では、会議を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) 型のパラメーターを受け取り、[PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトと [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) メソッドを使用して、**AppointmentItem** オブジェクトの [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) を取得します。 **EntryID** を取得した後、[GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) メソッドを使用して、会議の開催者を表す [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトを返します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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
        @"http://schemas.microsoft.com/mapi/proptag/0x00410102";
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

## <a name="see-also"></a>関連項目

- [会議出席依頼](meeting-requests.md)

