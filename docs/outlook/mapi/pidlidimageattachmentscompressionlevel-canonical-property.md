---
title: PidLidImageAttachmentsCompressionLevel 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357583"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a>PidLidImageAttachmentsCompressionLevel 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
画像の添付ファイルに適用する圧縮レベルを定義します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidImgAttchmtsCompressLevel  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x00008593  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>解説

有効な圧縮レベルは次のとおりです。
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]] 
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

