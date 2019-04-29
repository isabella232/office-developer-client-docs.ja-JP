---
title: メッセージサービスの構成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434509"
---
# <a name="configuring-a-message-service"></a>メッセージサービスの構成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **メッセージサービスのすべてのサービスプロバイダーを構成するには**
  
- [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出します。 構成に必要なすべてのデータがプログラムで利用できる場合は、ユーザーインターフェイスを表示するかどうかを選択できます。 ただし、1つまたは複数のプロバイダーの情報の一部を使用できない場合は、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS フラグを設定してください。 必要な構成データが利用できない場合にユーザーインターフェイスを非表示にすると、メッセージサービスは未構成の状態になります。
    
 **メッセージサービスで1つのサービスプロバイダーを構成するには**
  
1. 呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は、サービスプロバイダーの status オブジェクトにアクセスできます。 
    
2. 呼び出し[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)を呼び出して、サービスプロバイダーのプロパティシートを表示します。 
    
状態オブジェクトの使用の詳細については、「 [status Table and status objects](status-table-and-status-objects.md)」を参照してください。
  

