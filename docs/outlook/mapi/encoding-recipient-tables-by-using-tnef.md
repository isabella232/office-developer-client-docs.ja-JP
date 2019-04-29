---
title: TNEF を使用した受信者テーブルのエンコード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417960"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="be936-103">TNEF を使用した受信者テーブルのエンコード</span><span class="sxs-lookup"><span data-stu-id="be936-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="be936-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be936-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be936-105">ほとんどのメッセージングシステムは受信者リストを直接サポートしているため、TNEF ストリームへの受信者テーブルのエンコードはほとんど必要ありません。</span><span class="sxs-lookup"><span data-stu-id="be936-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="be936-106">通常、受信者のプロパティはメッセージヘッダーで送信されます。</span><span class="sxs-lookup"><span data-stu-id="be936-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="be936-107">受信者テーブルを含める必要がある場合、TNEF は通常の処理の一部として受信者テーブルをエンコードできます。</span><span class="sxs-lookup"><span data-stu-id="be936-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="be936-108">これは、TNEF 処理の初期段階で行われます。</span><span class="sxs-lookup"><span data-stu-id="be936-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="be936-109">トランスポートプロバイダーには、対象リストに指定されている**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを使用して[ITnef:: addprops](itnef-addprops.md)メソッドを呼び出すことによって、メッセージの受信者テーブルを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="be936-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="be936-110">tnef は、メッセージから受信者テーブルを取得し、その列セットをクエリして、テーブルの各行を TNEF ストリームに処理します。</span><span class="sxs-lookup"><span data-stu-id="be936-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="be936-111">代替メソッドは、エンコードされる前にトランスポートプロバイダーが受信者テーブルを変更する必要がある場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="be936-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="be936-112">トランスポートプロバイダーは必要なテーブルを作成し、 [ITnef:: EncodeRecips](itnef-encoderecips.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="be936-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="be936-113">_lpRecipTable_パラメーターで NULL が渡された場合、受信者テーブルは**ITnef:: addprops**の説明に従ってメッセージから直接取得されます。</span><span class="sxs-lookup"><span data-stu-id="be936-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

