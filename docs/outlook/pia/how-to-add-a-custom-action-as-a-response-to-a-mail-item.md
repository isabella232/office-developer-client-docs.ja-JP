---
title: メール アイテムへの返信として行うカスタム アクションを追加する
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6a82b02d357f86ca37d3ec4987ea6323d6d59cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359753"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a>メール アイテムへの返信として行うカスタム アクションを追加する

この例では、[Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)) コレクションの [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) メソッドを使用して、電子メール アイテムへの返信として実行するカスタム アクションの追加方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


カスタム アクションをプログラムで作成して、電子メールの返信のリボン (**[メッセージ]** タブの **[アクション]** グループ) に表示できます。 次のコード例の ReplyWithVoiceMail では、"Reply with Voice Mail" という名前のカスタムアクションを作成して、インスペクター コマンド バーに追加します。 ReplyWithVoiceMail では、最初に [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) オブジェクトを取得して、その **MailItem** に関連付けられた **Actions** コレクションの **Add** メソッドを呼び出すことで、[Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) オブジェクトを作成します。 その後、**Action** オブジェクトの [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) プロパティを "Reply with Voice Mail" に設定します。 [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\))、[ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\))、[CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\))、および [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) の各プロパティも設定します。 最後に、**MailItem** を保存します。


> [!NOTE]
> デザイン時に Outlook のフォーム デザイナーを使用してカスタム アクションを追加することもできます。


Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void ReplyWithVoiceMail()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.ActiveInspector().CurrentItem;
        Outlook.Action action = mail.Actions.Add();
        action.Name = “Reply with Voice Mail”;
        action.ReplyStyle = Outlook.OlActionReplyStyle.olUserPreference;
        action.ResponseStyle = Outlook.OlActionResponseStyle.olOpen;
        action.CopyLike = Outlook.OlActionCopyLike.olReply;
        action.MessageClass = “IPM.Post.Voice Message”;
        mail.Save();
    }
```

## <a name="see-also"></a>関連項目

- [メール](mail.md)

