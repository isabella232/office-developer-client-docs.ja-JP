---
title: メッセージサービスのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425394"
---
# <a name="copying-a-message-service"></a>メッセージサービスのコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **メッセージサービスをプロファイルにコピーするには**
  
- Call [IMsgServiceAdmin:: copymsgservice](imsgserviceadmin-copymsgservice.md)。
    
メッセージサービスがコピーされると、サービスの新しいインスタンスは元のインスタンスとまったく同じ方法で構成されます。 **copymsgservice**がエラー MAPI_E_ACCESS_DENIED を返す場合があります。 このエラーが返される最も一般的な原因は、メッセージサービスが重複して複製されないようにすることです。 
  

