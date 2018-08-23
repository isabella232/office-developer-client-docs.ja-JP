---
title: PidTagOriginalMessageClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a0abd3618f7a1586d8ca786fc1b6802c17e0f0f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573118"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a>PidTagOriginalMessageClass 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
レポートで使用する元のメッセージのクラスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIG_MESSAGE_CLASS、PR_ORIG_MESSAGE_CLASS_A、PR_ORIG_MESSAGE_CLASS_W  <br/> |
|識別子:  <br/> |0x004B  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージング プロパティをセキュリティで保護します。  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティには、レポートが生成されるメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティのコピーが含まれています。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

