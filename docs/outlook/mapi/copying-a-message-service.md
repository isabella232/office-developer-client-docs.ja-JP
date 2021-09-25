---
title: メッセージ サービスのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2f3f3d505d720fb00fabcad40761e573ecd47a45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617070"
---
# <a name="copying-a-message-service"></a>メッセージ サービスのコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **メッセージ サービスをプロファイルにコピーするには**
  
- [IMsgServiceAdmin::CopyMsgService を呼び出します](imsgserviceadmin-copymsgservice.md)。
    
メッセージ サービスをコピーすると、サービスの新しいインスタンスは元のインスタンスとまったく同じ方法で構成されます。 **CopyMsgService がエラー** メッセージを返MAPI_E_ACCESS_DENIED。 このエラーの戻り値の最も一般的な原因は、それ自体を複製できないメッセージ サービスです。 
  

