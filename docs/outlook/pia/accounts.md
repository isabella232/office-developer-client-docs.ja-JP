---
title: アカウント
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bd42bce785f79867e0f612fa65d43bd7eb1d078a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609174"
---
# <a name="accounts"></a>アカウント 

このセクションでは、電子メール アカウントに関連するサンプル タスクを示します。 電子メール アカウントの例は、Microsoft Exchange Server、Post Office Protocol 3 (POP3)、Internet Message Access Protocol (IMAP)、および Hypertext Transfer Protocol (HTTP) のアカウントです。 現在のプロファイルのアカウントは、[Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) オブジェクトによって表されます。


|トピック|説明|
|:----|:----------|
|[アカウント情報を取得する](how-to-get-account-information.md) | 信頼されている Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) オブジェクトを入力引数として受け取り、 **Account** オブジェクトを使用して、現在の Outlook プロファイルで使用できる各アカウントの詳細を表示します。|
|[現在のフォルダーに基づいて特定のアカウントの送信可能なアイテムを作成する](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | 送信可能な電子メール アイテムと会議出席依頼を作成する方法と、それらを現在のフォルダーに基づく特定のアカウントを使用して送信する方法を示す 2 つのコード例が含まれています。|
|[フォルダーのアカウントを取得する](how-to-get-the-account-for-a-folder.md) | 現在のセッションで特定のフォルダーに関連付けられているアカウントを取得します。|
|[複数のアカウントの情報を取得する](how-to-get-information-about-multiple-accounts.md) | 現在のプロファイルの各アカウントの情報を取得して表示します。|
|[Hotmail アカウントを使用してメール アイテムを送信する](how-to-send-a-mail-item-by-using-a-hotmail-account.md) | [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) プロパティを使用し、Windows Live Hotmail アカウントを使用して、メール アイテムを送信します。|

## <a name="see-also"></a>関連項目

- [Exchange ユーザー](exchange-users.md)
- [メール](mail.md)
- [受信者](recipients.md)
- [操作方法 (Outlook 2013 PIA リファレンス)](how-do-i-outlook-2013-pia-reference.md)

