---
title: web サーバーコンピューターへのゲスト権限の付与RDS ゲストの権限
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292126"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>web サーバーコンピューターへのゲスト権限の付与RDS ゲストの権限

**適用先:** Access 2013、Office 2013

RDS を使用するには、\_web サーバーコンピューターの Guests ローカルグループに匿名 web サーバーアカウント (IUSR*ComputerName*) を追加する必要があります。

**web サーバーコンピューターへのゲスト権限を付与するには**

1.  Microsoft Windows 2000 Server コンピューターで、[**スタート**] をクリックし、[**プログラム**]、[**管理ツール**] の順にポイントし、[**コンピューターの管理**] をクリックします。

2.  In the console tree, in **Local Users and Groups**, click **Groups**.

3.  Select the **Guests** local group. From the **Action** menu, choose **Properties**.

4.  In the **Guests Properties** dialog box, click **Add**.

5.  匿名 web サーバーアカウントが **[ユーザーまたはグループの選択**] ダイアログボックスの一覧に表示されない場合は、その\_名前 (IUSR*ComputerName*) を下部の空のボックスに入力し、[**追加**] をクリックします。

6.  **[OK]** をクリックします。

