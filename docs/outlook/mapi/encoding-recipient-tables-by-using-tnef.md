---
title: TNEF を使用した受信者テーブルのエンコード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8110eff9b38c76023621f34396d65714a4316d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800014"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="de8aa-103">TNEF を使用した受信者テーブルのエンコード</span><span class="sxs-lookup"><span data-stu-id="de8aa-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="de8aa-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de8aa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de8aa-105">TNEF ストリームに、受信者テーブルのエンコーディングは、多くのメッセージング システムの受信者の一覧を直接サポートするために必要はほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="de8aa-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="de8aa-106">一般に、受信者のプロパティは、メッセージのヘッダーで送信されます。</span><span class="sxs-lookup"><span data-stu-id="de8aa-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="de8aa-107">受信者テーブルを含めることが必要な場合は、TNEF は、通常の処理の一部として受信者テーブルをエンコードできます。</span><span class="sxs-lookup"><span data-stu-id="de8aa-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="de8aa-108">これは、は、TNEF の処理の初期段階で行われます。</span><span class="sxs-lookup"><span data-stu-id="de8aa-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="de8aa-109">トランスポート プロバイダーは、信頼のリストで指定されている**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを使用して、 [ITnef::AddProps](itnef-addprops.md)メソッドを呼び出すことによって、メッセージの受信者テーブルを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="de8aa-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="de8aa-110">TNEF は、メッセージの受信者テーブルを取得、列セットに対してクエリを実行し、TNEF ストリームに、テーブルのすべての行を処理します。</span><span class="sxs-lookup"><span data-stu-id="de8aa-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="de8aa-111">別の方法では、トランスポート プロバイダーをエンコードする前に、受信者テーブルを変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="de8aa-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="de8aa-112">トランスポート プロバイダーは、必要なテーブルを作成し、 [ITnef::EncodeRecips](itnef-encoderecips.md)メソッドを呼び出してできます。</span><span class="sxs-lookup"><span data-stu-id="de8aa-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="de8aa-113">_LpRecipTable_パラメーターに NULL を渡した場合、受信者テーブルから直接取得されますメッセージ**ITnef::AddProps**で説明されているようです。</span><span class="sxs-lookup"><span data-stu-id="de8aa-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

