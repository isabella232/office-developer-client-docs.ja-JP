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
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="151ca-102">web サーバーコンピューターへのゲスト権限の付与RDS ゲストの権限</span><span class="sxs-lookup"><span data-stu-id="151ca-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="151ca-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="151ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="151ca-104">RDS を使用するには、\_web サーバーコンピューターの Guests ローカルグループに匿名 web サーバーアカウント (IUSR*ComputerName*) を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="151ca-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="151ca-105">**web サーバーコンピューターへのゲスト権限を付与するには**</span><span class="sxs-lookup"><span data-stu-id="151ca-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="151ca-106">Microsoft Windows 2000 Server コンピューターで、[**スタート**] をクリックし、[**プログラム**]、[**管理ツール**] の順にポイントし、[**コンピューターの管理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="151ca-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="151ca-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span><span class="sxs-lookup"><span data-stu-id="151ca-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="151ca-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span><span class="sxs-lookup"><span data-stu-id="151ca-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="151ca-110">In the **Guests Properties** dialog box, click **Add**.</span><span class="sxs-lookup"><span data-stu-id="151ca-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="151ca-111">匿名 web サーバーアカウントが **[ユーザーまたはグループの選択**] ダイアログボックスの一覧に表示されない場合は、その\_名前 (IUSR*ComputerName*) を下部の空のボックスに入力し、[**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="151ca-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="151ca-112">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="151ca-112">Click **OK**.</span></span>

