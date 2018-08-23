---
title: PidTagProviderSubmitTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e08b56fcfea38bf65e8628acfa481716554e2c01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571613"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a>PidTagProviderSubmitTime 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート プロバイダーでは、その基になるメッセージング システムにメッセージが渡されるときの日時が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_SUBMIT_TIME  <br/> |
|識別子:  <br/> |0x0048  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージの送信時に送信トランスポート プロバイダーによって設定が。
  
このプロパティは、X.400 送信エンベロープ メッセージごとの属性に対応します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

