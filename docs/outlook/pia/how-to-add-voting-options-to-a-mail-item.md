---
title: メール アイテムに投票オプションを追加する
TOCTitle: Add voting options to a mail item
ms:assetid: 0fb209a8-178d-411e-9551-0a72e041fd65
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424466(v=office.15)
ms:contentKeyID: 55119867
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3befe70363d1e2226b8a3a3a6ebb8db39aa2c6ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359725"
---
# <a name="add-voting-options-to-a-mail-item"></a>メール アイテムに投票オプションを追加する

この例では、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトの [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) プロパティを使用して、電子メール メッセージに投票オプションを追加する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


メッセージの投票オプションは、メッセージ受信者に選択肢の一覧を示して回答を追跡するために使用します。投票オプションをプログラムで作成するには、値の一覧をセミコロン区切りで記述した文字列を **MailItem** オブジェクトの **VotingOptions** プロパティに設定します。 **VotingOptions** プロパティの値は、受信メッセージのリボンの [ **返信**] グループの [ **投票**] コマンドに表示されます。

次の例の OrderPizza は、新しいメール メッセージに投票オプションを作成します。 OrderPizza は、まず **MailItem** を作成し、**VotingOptions** プロパティを "Cheese; Mushroom; Sausage; Combo; Veg Combo" に設定して、[Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) プロパティを "Pizza Order" に設定します。 "Pizza Order" メッセージを送信すると、受信者には投票オプションが表示されます。 回答を受診するたびに、差出人の送信済みアイテム フォルダーのメッセージの **[追跡]** ページに、受診者の選択内容が集計されます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void OrderPizza()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.CreateItem(
            Outlook.OlItemType.olMailItem);
        mail.VotingOptions = “Cheese; Mushroom; Sausage; Combo; Veg Combo;”
        mail.Subject = “Pizza Order”;
        mail.Display(false);
    }
```

## <a name="see-also"></a>関連項目

- [メール](mail.md)

