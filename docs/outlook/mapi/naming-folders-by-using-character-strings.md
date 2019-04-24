---
title: 文字列を使用してフォルダーに名前を付ける
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326251"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="cd89b-103">文字列を使用してフォルダーに名前を付ける</span><span class="sxs-lookup"><span data-stu-id="cd89b-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="cd89b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd89b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd89b-105">セッション中に頻繁に1つ以上のフォルダーにアクセスする場合は、 [IMsgStore:: setreceivefolder](imsgstore-setreceivefolder.md)メソッドを使用してフォルダーに名前を割り当てることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="cd89b-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="cd89b-106">**IMsgStore:: setreceivefolder**は、主に特定のメッセージクラスに対する受信メッセージを受信する特別なフォルダーを確立するために使用されますが、任意のフォルダーを名前に関連付けるためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="cd89b-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="cd89b-107">この名前は、メッセージクラスと同じにすることも、クライアントの使用に合わせてカスタマイズされた任意の文字文字列にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cd89b-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="cd89b-108">フォルダーに名前を関連付けると、フォルダーを見つけて開くのにかかる時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="cd89b-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

