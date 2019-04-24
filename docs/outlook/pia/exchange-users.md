---
title: Exchange ユーザー
TOCTitle: Exchange users
ms:assetid: 01802032-fd60-400b-ad83-1f4eefe596bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184585(v=office.15)
ms:contentKeyID: 55119835
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 667f8a07477c527d251c4e50f35baa2da2e417ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357835"
---
# <a name="exchange-users"></a>Exchange ユーザー

このセクションでは、Microsoft Exchange メールボックス ユーザーに関連するサンプル タスクを示します。Exchange ユーザーは、Exchange Server に接続しているユーザーで、[ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトで表されます。これらのオブジェクトは [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトから派生します。

## <a name="in-this-section"></a>このセクションの内容

|トピック|説明|
|:----|:----------|
|[現在のユーザーの情報を取得する](how-to-get-information-about-the-current-user.md)  |名前、役職、電話番号など、現在のユーザーの情報を取得します。|
|[現在のユーザーがメンバーになっているすべての配布リストについての情報を取得する](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)  |[GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) メソッドを使用して、現在のユーザーがメンバーになっているすべての配布リストについての情報を取得します。|
|[配布リストを作成する](how-to-create-a-distribution-list.md)  |配布リストを作成し、それをユーザーに表示します。|
[Exchange 配布リストのメンバーを取得する](how-to-get-members-of-an-exchange-distribution-list.md)  |ユーザーが [ **名前の選択**] ダイアログ ボックスで Exchange 配布リストを選択できるようにして、配布リストを展開してリストのメンバーを表示します。|
[現在のユーザーの上司の情報を取得する](how-to-get-information-about-the-current-user-s-manager.md)  |現在のユーザーの上司についての情報 (名前、役職、電話番号など) を取得します。|
[Exchange ユーザーの上司の空き時間情報を取得する](how-to-get-availability-information-for-an-exchange-user-s-manager.md) |  ユーザーの上司の予定表で次に空いている 60 分の時間枠を表示します。|
|[会議出席依頼に対する上司からの返信を確認する](how-to-check-a-manager-s-response-to-a-meeting-request.md) | [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドおよび [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) メソッドを使用して、会議出席依頼に対する現在のユーザーの上司からの返信の状態を確認します。|
|[現在のユーザーの上司の直属部下についての情報を取得する](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md) | 現在のユーザーに上司がいる場合はその上司の直属の部下を取得し、上司の各直属部下についての情報を表示します。|

## <a name="see-also"></a>関連項目

- [アカウント](accounts.md)
- [アドレス帳](address-book.md)
- [ストア](stores.md)
- [操作方法 (Outlook 2013 PIA リファレンス)](how-do-i-outlook-2013-pia-reference.md)

