---
title: Web サーバー コンピューターにゲストの特権を付与します。RDS ゲスト権限
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d09de280c9edcfdf4305bb6c2ba09aa01e556ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478174"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Web サーバー コンピューターにゲストの特権を付与します。RDS ゲスト権限 


**適用されます**Access 2013 |。Office 2013

Web サーバーの匿名アカウント (IUSR\_*コンピューター名*) RDS を使用する Web サーバー コンピューターの Guests ローカル グループに追加する必要があります

**Web サーバー コンピューターへのゲスト権限でのアクセスを許可するには**

1.  Microsoft Windows® 2000 Server コンピューターに [**スタート**] ボタン、**プログラム**] をポイント **[管理ツール**] をポイントし、[**コンピューターの管理**] をクリックします。

2.  コンソール ツリーで、**ローカル ユーザーとグループ**は、[**グループ**] をクリックします。

3.  **Guests**ローカル グループを選択します。 **[操作**] メニューから**プロパティ**を選択します。

4.  **Guests のプロパティ**] ダイアログ ボックスで、[**追加**を] をクリックします。

5.  匿名 Web サーバー アカウントが **[ユーザーまたはグループ**] ダイアログ ボックスの一覧に表示されない場合は、その名前を入力 (IUSR\_*コンピューター名*) 空白の下にボックスし、[**追加**] をクリックします。

6.  **[OK]** をクリックします。

