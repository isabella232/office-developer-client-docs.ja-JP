---
title: PidTagSupplementaryInfo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIi.PidTagSupplementaryInfo
api_type:
- COM
ms.assetid: 2d4231b5-4096-4c0d-b694-65e2d04172b8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: de9635fa77cd0c282723e0f76eabd6bc0d0dbab9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339348"
---
# <a name="pidtagsupplementaryinfo-canonical-property"></a>PidTagSupplementaryInfo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レポートで使用する追加情報が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUPPLEMENTARY_INFO、PR_SUPPLEMENTARY_INFO_A、PR_SUPPLEMENTARY_INFO_W  <br/> |
|識別子:  <br/> |0x0c1b  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティには、メッセージ転送エージェントまたはレポートに関連するトランスポートプロバイダーによって生成される情報が含まれています。 これは、通常、基になるメッセージングシステムで発生した配信レポートまたは配信不能レポートテキストに使用されます。
  
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

