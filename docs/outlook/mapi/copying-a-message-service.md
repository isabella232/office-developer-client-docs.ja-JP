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
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573720"
---
# <a name="copying-a-message-service"></a>メッセージ サービスのコピー

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 **メッセージ サービスをプロファイルにコピーするには**
  
- [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md)を呼び出します。
    
メッセージ サービスをコピーすると、サービスの新しいインスタンスがオリジナルと全く同じように構成します。 場合があります**CopyMsgService**では、MAPI_E_ACCESS_DENIED エラーが返されます。 このエラーの戻り値の最も一般的な原因は、自身を複製するのには許可されていないメッセージ サービスです。 
  

