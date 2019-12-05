---
title: 電子名刺のレイアウトを変更する
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-modify-the-layout-of-an-electronic-business-card?redirectedfrom=MSDN
ms:contentKeyID: 55119838
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a0592be61def24fc1d8cd50e82ebdfea1ed9d624
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819323"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>電子名刺のレイアウトを変更する

この例では、[ContactItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.contactitem?redirectedfrom=MSDN&view=outlook-pia) インターフェイスの [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) プロパティを使用して、電子名刺のレイアウトを変更する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

電子名刺には、連絡先から特定の情報をキャプチャする連絡先ビューが示されます。 **ContactItem** インターフェイスは、電子名刺に関連する特定のメンバーを提供します。 そのメンバーとは、**BusinessCardLayoutXml**、[BusinessCardType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.businesscardtype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_BusinessCardType)、[AddBusinessCardLogoPicture(String)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.addbusinesscardlogopicture?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_AddBusinessCardLogoPicture_System_String_)、[ForwardAsBusinessCard()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.forwardasbusinesscard?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ForwardAsBusinessCard)、[ResetBusinessCard()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.resetbusinesscard?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ResetBusinessCard)、[SaveBusinessCardImage(String)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.savebusinesscardimage?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_SaveBusinessCardImage_System_String_)、および [ShowBusinessCardEditor()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.showbusinesscardeditor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ShowBusinessCardEditor) です。

次のコード例では、電子名刺のレイアウトを変更するために、まず、BusinessCardLayoutExample で **ContactItem** オブジェクトを取得します。 この例の場合、**ContactItem** は [Subject](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.subject?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_Subject) プロパティの値が "Melissa MacBeth" と一致する連絡先です。 その次に、BusinessCardLayoutExample で XML ドキュメント クラス [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k) を作成して、このクラスの layout 属性を文字列で取得するために **ContactItem** オブジェクトの **BusinessCardLayoutXML** 値を使用します。 その後で、カードのレイアウトを左揃えから右揃えに変更します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [電子名刺](electronic-business-cards.md)

