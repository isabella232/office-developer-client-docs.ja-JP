---
title: 文字の文字列を使用してフォルダーの名前付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801662"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="34d28-103">文字の文字列を使用してフォルダーの名前付け</span><span class="sxs-lookup"><span data-stu-id="34d28-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="34d28-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34d28-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34d28-105">セッション中に頻繁に 1 つまたは複数のフォルダーにアクセスする場合は、 [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)メソッドを使用してフォルダーに名前を割り当てることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="34d28-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="34d28-106">**IMsgStore::SetReceiveFolder**を使用して、特定のメッセージ クラスのメッセージを受信する特別なフォルダーを設定するには、主に、名前を持つ任意のフォルダーを関連付けるには、使用できます。</span><span class="sxs-lookup"><span data-stu-id="34d28-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="34d28-107">メッセージ クラスと同じ名前は、または任意の文字列をクライアントの使用に合わせてカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="34d28-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="34d28-108">フォルダーに名前を関連付けることを検索して、フォルダーを開くにかかる時間が減少します。</span><span class="sxs-lookup"><span data-stu-id="34d28-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

