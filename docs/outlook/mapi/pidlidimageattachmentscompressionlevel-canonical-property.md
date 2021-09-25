---
title: PidLidImageAttachmentsCompressionLevel 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bceb1a75cbca5ee92de449c8d36e175131470143
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555763"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a>PidLidImageAttachmentsCompressionLevel 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イメージ添付ファイルに適用する圧縮レベルを定義します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidImgAttchmtsCompressLevel  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008593  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>注釈

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

[[MS-OXPROPS]] 
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

