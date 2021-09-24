---
title: 非表示メッセージとしてフォルダーに格納されているソリューション固有のデータにアクセスする
TOCTitle: Access solution-specific data stored as a hidden message in a folder
ms:assetid: bacf0562-1026-4c3b-87b0-4eaad5033592
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623414(v=office.15)
ms:contentKeyID: 55119861
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 03d2fd590f2b5c6eefdaec691a5ee25e9431f59f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549729"
---
# <a name="access-solution-specific-data-stored-as-a-hidden-message-in-a-folder"></a>非表示メッセージとしてフォルダーに格納されているソリューション固有のデータにアクセスする

この例では、[StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) オブジェクトを使用して、特定のメッセージ クラスの非表示メッセージとしてフォルダーに格納されているデータを取得する方法を示します。

## <a name="example"></a>例

**StorageItem** オブジェクトは、通常、プログラムでは表示できないソリューション固有のデータを非表示にするために使用されます。Exchange 環境では、 **StorageItem** オブジェクトは、ソリューションの設定を移動し、その設定がオンラインでもオフラインでも使用できることを保証するために使用されます。カスタム メッセージ クラスを **StorageItem** オブジェクトに割り当てることも、オブジェクトを件名で識別することもできます。

次のコード サンプルでは、予定表フォルダーに非表示メッセージとして格納されていて メッセージ クラスが IPM.Configuration.WorkHours である XML データを取得します。

[PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトは、XML の文字列表現ではなく、バイト ストリームを含むオブジェクトとして XML を返します。このコード サンプルでは、 **System.Text.Encoding.Ascii.GetString** を使用してバイト ストリームを文字列に変換します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Function GetWorkHoursXML() As String
    Try
        Dim storage As Outlook.StorageItem = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage( _
            "IPM.Configuration.WorkHours", _
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass)
        Dim pa As Outlook.PropertyAccessor = storage.PropertyAccessor
        ' PropertyAccessor will return a byte array for this property
        Dim rawXmlBytes As Byte() = CType(pa.GetProperty( _
            "http://schemas.microsoft.com/mapi/proptag/0x7C080102"), _
            Byte())
        ' Use Encoding to convert the array to a string
        Return System.Text.Encoding.ASCII.GetString(rawXmlBytes)
    Catch
        Return String.Empty
    End Try
End Function
```

```csharp
private string GetWorkHoursXML()
{
    try
    {
        Outlook.StorageItem storage =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage(
            "IPM.Configuration.WorkHours",
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass);
        Outlook.PropertyAccessor pa = storage.PropertyAccessor;
        // PropertyAccessor will return a byte array for this property
        byte[] rawXmlBytes = (byte[])pa.GetProperty(
            "http://schemas.microsoft.com/mapi/proptag/0x7C080102");
        // Use Encoding to convert the array to a string
        return System.Text.Encoding.ASCII.GetString(rawXmlBytes);
    }
    catch
    {
        return string.Empty;
    }
}
```


## <a name="see-also"></a>関連項目

- [フォルダー](folders.md)

