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
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="93f1a-102">Web サーバー コンピューターにゲストの特権を付与します。RDS ゲスト権限</span><span class="sxs-lookup"><span data-stu-id="93f1a-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="93f1a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="93f1a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="93f1a-104">Web サーバーの匿名アカウント (IUSR\_*コンピューター名*) RDS を使用する Web サーバー コンピューターの Guests ローカル グループに追加する必要があります</span><span class="sxs-lookup"><span data-stu-id="93f1a-104">The anonymous Web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the Web server computer to use RDS.</span></span>

<span data-ttu-id="93f1a-105">**Web サーバー コンピューターへのゲスト権限でのアクセスを許可するには**</span><span class="sxs-lookup"><span data-stu-id="93f1a-105">**To grant guest privileges to a Web server computer**</span></span>

1.  <span data-ttu-id="93f1a-106">Microsoft Windows® 2000 Server コンピューターに [**スタート**] ボタン、**プログラム**] をポイント **[管理ツール**] をポイントし、[**コンピューターの管理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93f1a-106">On your Microsoft Windows® 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="93f1a-107">コンソール ツリーで、**ローカル ユーザーとグループ**は、[**グループ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93f1a-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="93f1a-108">**Guests**ローカル グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="93f1a-108">Select the **Guests** local group.</span></span> <span data-ttu-id="93f1a-109">**[操作**] メニューから**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="93f1a-109">From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="93f1a-110">**Guests のプロパティ**] ダイアログ ボックスで、[**追加**を] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93f1a-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="93f1a-111">匿名 Web サーバー アカウントが **[ユーザーまたはグループ**] ダイアログ ボックスの一覧に表示されない場合は、その名前を入力 (IUSR\_*コンピューター名*) 空白の下にボックスし、[**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93f1a-111">If the anonymous Web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="93f1a-112">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93f1a-112">Click **OK**.</span></span>

