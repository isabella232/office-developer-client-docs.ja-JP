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
ms.openlocfilehash: c5e840250da7ba3b95150f2e83e1eb08b0c61ab5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286423"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a>PidTagProviderSubmitTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーが、基になるメッセージングシステムにメッセージを渡した日時を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_SUBMIT_TIME  <br/> |
|識別子:  <br/> |0x0048  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |MAPI エンベロープ  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージの送信時に、送信トランスポートプロバイダーによって設定されます。
  
このプロパティは、メッセージごとの400送信エンベロープ属性に対応します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

