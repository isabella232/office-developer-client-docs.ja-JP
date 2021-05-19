---
title: フォルダーの既定のメッセージ クラスを取得する
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 031b7736ed397b9218ea677442f80595da2aa919
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542563"
---
# <a name="get-the-default-message-class-of-a-folder"></a>フォルダーの既定のメッセージ クラスを取得する

この例では、[DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) プロパティを使用してフォルダーの既定のメッセージ クラスを取得する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

フォルダーの既定のメッセージ クラスを取得するには、[MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) オブジェクトの **DefaultMessageClass** プロパティを使用します。 たとえば、[Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトの **DefaultMessageClass** が IPM.Contact であれば、Contact フォルダーを表します。 しかし、フォルダーの既定のフォームがカスタム フォームまたは代替フォームの場合は、 [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトを使用して既定のフォームのメッセージ クラスを決定する必要があります。 **DefaultMessageClass** プロパティはフォルダーの既定のフォームのメッセージ クラスを返しません。

次のコード例では、GetDefaultMessageClass プロシージャが **PropertyAccessor** を使用してフォルダーの既定のフォームを決定します。 フォルダー プロパティ **PR \_ DEF POST \_ \_ MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\))が見つからない場合、Outlookエラーが発生する場合は **、try..。catch** ブロックは **、Folder の DefaultMessageClass** プロパティを返 **します**。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"http://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a>関連項目

- [フォルダー](folders.md)

