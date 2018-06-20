---
title: メッセージ サービスのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799808"
---
# <a name="copying-a-message-service"></a>メッセージ サービスのコピー

  
  
**適用されます**: Outlook 
  
 **メッセージ サービスをプロファイルにコピーするには**
  
- [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md)を呼び出します。
    
メッセージ サービスをコピーすると、サービスの新しいインスタンスがオリジナルと全く同じように構成します。 場合があります**CopyMsgService**では、MAPI_E_ACCESS_DENIED エラーが返されます。 このエラーの戻り値の最も一般的な原因は、自身を複製するのには許可されていないメッセージ サービスです。 
  

