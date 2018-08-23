---
title: 'title: "��\���ɂ��� MAPI �t�H���_�[" ms.author: v-tirob author: v-tirob manager: soliver ms.date: 11/16/2014 ms.audience: Developer ms.topic: overview ms.prod: office-online-server localization_priority: Normal api_type:'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: 'COM ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1 description: "�ŏI�X�V��: 2011�N7��23��"'
ms.openlocfilehash: 81b53bc138a64da673d6723e60fd90b086174efe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801381"
---
# <a name="mapi-hidden-folders"></a><span data-ttu-id="aa4e0-103">��\���ɂ��� MAPI �t�H���_�[</span><span class="sxs-lookup"><span data-stu-id="aa4e0-103">MAPI Hidden Folders</span></span>

  
  
<span data-ttu-id="aa4e0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa4e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa4e0-105">隠しフォルダーは、クライアントは、メッセージ ・ ストアのルート フォルダーではなく、個人間メッセージ (IPM) サブツリーのルート フォルダーを作成する一般的なフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="aa4e0-105">Hidden folders are generic folders that clients create in the root folder of the message store, rather than in the root folder of an interpersonal message (IPM) subtree.</span></span> <span data-ttu-id="aa4e0-106">これらのフォルダーが、IPM サブツリーに配置されていないため一般にによって隠されているユーザーのビューから、メッセージ ストア プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="aa4e0-106">Because these folders are not placed in an IPM subtree, they are generally hidden from the user's view by the message store provider.</span></span> <span data-ttu-id="aa4e0-107">隠しフォルダーには、通常は、メッセージ ・ ストアに関連するが、ユーザーに関係のない情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="aa4e0-107">Hidden folders typically contain information that is relevant to the message store but irrelevant to the user.</span></span> <span data-ttu-id="aa4e0-108">クライアントは、たとえば、フォルダー階層の残りの部分を保存する追加情報を格納するフォルダーを非表示を作成します。</span><span class="sxs-lookup"><span data-stu-id="aa4e0-108">Clients create hidden folders to store, for example, additional information to be saved with the rest of the folder hierarchy.</span></span>
  
<span data-ttu-id="aa4e0-109">MAPI には、表示、作成、変更、および、IPM サブツリー内のフォルダーを削除することができるすべてのクライアントが期待しています。</span><span class="sxs-lookup"><span data-stu-id="aa4e0-109">MAPI expects all clients to be able to display, create, modify, and delete folders in an IPM subtree.</span></span> <span data-ttu-id="aa4e0-110">他のツリー内のフォルダーを操作するためのサポートは、省略可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="aa4e0-110">Support for working with folders in other trees is considered optional.</span></span> <span data-ttu-id="aa4e0-111">ただし、既定のストアとして使用できるものと、メッセージを送受信するすべてのメッセージ ストアは、非表示のフォルダーを完全にサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa4e0-111">However, all message stores that can be used as the default store and that can send and receive messages should fully support hidden folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa4e0-112">�֘A����</span><span class="sxs-lookup"><span data-stu-id="aa4e0-112">See also</span></span>



<span data-ttu-id="aa4e0-113">[MAPI �t�H���_�[](mapi-folders.md)</span><span class="sxs-lookup"><span data-stu-id="aa4e0-113">[MAPI Folders](mapi-folders.md)</span></span>

