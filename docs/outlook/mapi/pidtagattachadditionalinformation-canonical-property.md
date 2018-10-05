---
title: PidTagAttachAdditionalInformation 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389632"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a>PidTagAttachAdditionalInformation 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Windows 以外の添付ファイルのファイルの種類の情報を提供します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_ADDITIONAL_INFO  <br/> |
|識別子:  <br/> |0x370F  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、添付ファイルのエンコーディングに基づいて、特定の添付ファイルに関するメタデータを提供します。 たとえば、 **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) のプロパティには、MacBinary が含まれている、 **PR_ATTACH_ADDITIONAL_INFO**が含まれています、Macintosh のファイルの作成者とファイルの種類を":CREA:TYPE"として書式設定を表す文字列にはエンコード済みの Macintosh のファイルです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

