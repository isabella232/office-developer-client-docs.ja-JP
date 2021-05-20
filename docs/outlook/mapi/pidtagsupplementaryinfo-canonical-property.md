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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de9635fa77cd0c282723e0f76eabd6bc0d0dbab9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429755"
---
# <a name="pidtagsupplementaryinfo-canonical-property"></a>PidTagSupplementaryInfo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レポートで使用する追加情報が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUPPLEMENTARY_INFO、PR_SUPPLEMENTARY_INFO_A、PR_SUPPLEMENTARY_INFO_W  <br/> |
|識別子:  <br/> |0x0C1B  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティには、レポートに関連するメッセージ転送エージェントまたはトランスポート プロバイダーによって生成される情報が含まれています。 これは通常、基になるメッセージング システムで発生した配信または配信以外のレポート テキストに使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

