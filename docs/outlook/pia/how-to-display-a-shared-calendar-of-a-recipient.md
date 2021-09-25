---
title: 受信者の共有の予定表を表示する
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5775c7856ecf5d4e163f5c27e9aeca3ab55920bb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560607"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a>受信者の共有の予定表を表示する

この例では、[CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) メソッドと [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) メソッドを使用して、受信者の共有の予定表を表示する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトなどの送信可能なアイテムは、常に [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) プロパティを公開します。このプロパティを使用することで、送信可能なアイテムの [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) コレクションにアクセスできます。アイテムの [Recipients](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) コレクションにバインドされていない **Recipient** オブジェクトを作成するには、 [NameSpace](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) オブジェクトの [CreateRecipient(String)](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) メソッドを使用します。次に、このバインドされていない **Recipient** オブジェクトを [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) メソッドに渡すと、このメソッドから共有の Exchange フォルダーが返されます。これで、共有の Exchange フォルダーを開き、エクスプローラー ウィンドウにそのフォルダーを表示することができます。 GetSharedDefaultFolder は、代理人が委任元のフォルダーへのアクセスを許可されている Exchange 代理シナリオで使用します。 **Recipient** オブジェクトは、 GetSharedDefaultFolder メソッドに渡す前に解決しておく必要があります。 **Recipient** オブジェクトを解決するには、そのオブジェクトの [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) メソッドを呼び出します。

次のコード例では、DisplayManagerCalendar が、**CreateRecipient** と **GetSharedDefaultFolder** を呼び出して、現在のユーザーのマネージャーの予定表フォルダーを開き、表示します。ユーザーにマネージャーの予定表フォルダーを開く権限がない、またはエラーが発生すると、通知ダイアログ ボックスが表示されます。


> [!NOTE]
> **Namespace** オブジェクトの **CreateRecipient** メソッド、または **Recipients** コレクションの [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) メソッドを使用して **Recipient** オブジェクトを作成する場合は、受信者の名前を提供する必要があります。 **Recipient** は、この名前に対して解決されます。 受信者の名前は、次のいずれかの形式をにすることができます。
> - 表示名
> - エイリアス
> - 簡易メール転送プロトコル (SMTP) アドレス

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayManagerCalendar()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.Recipient recip =
                Application.Session.CreateRecipient(manager.Name);
            if (recip.Resolve())
            {
                try
                {
                    Outlook.Folder folder =
                        Application.Session.GetSharedDefaultFolder(
                        recip, Outlook.OlDefaultFolders.olFolderCalendar)
                        as Outlook.Folder;
                    folder.Display();
                }
                catch
                {
                    MessageBox.Show("Could not open manager's calendar.",
                        "GetSharedDefaultFolder Example",
                        MessageBoxButtons.OK,
                        MessageBoxIcon.Error);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [予定表](calendar.md)

