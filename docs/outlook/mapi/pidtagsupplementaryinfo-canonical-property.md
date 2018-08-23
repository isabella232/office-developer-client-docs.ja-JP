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
ms.openlocfilehash: f9800b1822ca6881c451e01e890d582c77b64546
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566748"
---
# <a name="pidtagsupplementaryinfo-canonical-property"></a>PidTagSupplementaryInfo 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
レポートで使用するための追加情報が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUPPLEMENTARY_INFO、PR_SUPPLEMENTARY_INFO_A、PR_SUPPLEMENTARY_INFO_W  <br/> |
|識別子:  <br/> |0x0C1B  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティには、メッセージ転送エージェントによって生成される情報が含まれているか、トランスポート プロバイダーは、レポートに関連します。 配信または配信不能レポートのテキストの基になるメッセージング システムに送信された場合に通常使用されます。
  
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

