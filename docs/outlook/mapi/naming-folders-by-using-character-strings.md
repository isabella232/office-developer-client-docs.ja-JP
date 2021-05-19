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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428313"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="11ffd-103">文字列を使用してフォルダーに名前を付ける</span><span class="sxs-lookup"><span data-stu-id="11ffd-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="11ffd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11ffd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11ffd-105">セッション中に頻繁に 1 つ以上のフォルダーにアクセスする場合は [、IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) メソッドを使用してフォルダーに名前を割り当てすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="11ffd-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="11ffd-106">**IMsgStore::SetReceiveFolder** は、主に特定のメッセージ クラスの受信メッセージを受信するための特別なフォルダーを確立するために使用しますが、任意のフォルダーを名前に関連付ける場合にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="11ffd-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="11ffd-107">名前はメッセージ クラスと同じにするか、クライアントの使用に合わせてカスタマイズされた任意の文字列を指定できます。</span><span class="sxs-lookup"><span data-stu-id="11ffd-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="11ffd-108">名前をフォルダーに関連付けすると、フォルダーを検索して開くのにかかる時間が減少します。</span><span class="sxs-lookup"><span data-stu-id="11ffd-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

