---
title: TNEF によるユーザー設定処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c015335a-8fcd-4b03-abb9-9b6b72000e13
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3ee219ec09116640903df75ce271f607972dd37e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430848"
---
# <a name="custom-processing-with-tnef"></a><span data-ttu-id="66555-103">TNEF によるユーザー設定処理</span><span class="sxs-lookup"><span data-stu-id="66555-103">Custom processing with TNEF</span></span>

<span data-ttu-id="66555-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66555-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66555-105">トランスポートプロバイダーは、カスタム処理を使用して、添付ファイル自体のプロパティを処理したり、添付ファイルを個別に送信したり、メッセージングシステムの添付モデルを介して送信したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="66555-105">Transport providers can use custom processing to process the properties on an attachment itself, transmit attachments separately, or transmit them through the messaging system's attachment model.</span></span> <span data-ttu-id="66555-106">TNEF は、トランスポートプロバイダーがメッセージとは別に添付ファイルを送信し、それらを受信側に再接続できるようにするメカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="66555-106">TNEF uses a mechanism that enables the transport provider to send the attachments apart from the message and reconnect them on the receiving side.</span></span>
  

