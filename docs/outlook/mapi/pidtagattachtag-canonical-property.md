---
title: PidTagAttachTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8ba391d81a9a615c2c80bc44e429e388e9a50779
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579195"
---
# <a name="pidtagattachtag-canonical-property"></a>PidTagAttachTag 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルを指定したアプリケーションを指定する ASN.1 オブジェクト識別子が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_TAG  <br/> |
|識別子:  <br/> |0x370A  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、最初に添付ファイルを生成したアプリケーションを識別します。
  
 **メモ** プロパティ **PR_ATTACH_ENCODING** [(PidTagAttachEncoding)](pidtagattachencoding-canonical-property.md)とPR_ATTACH_TAG **プロパティは** 混同しないでください。 これらはペアまたは関連付けではありません。 **PR_ATTACH_ENCODING、** 添付ファイル内のデータを変換するために使用されるアルゴリズムを識別します。 "Object" はオブジェクト識別子という用語で、X.400 使用法ではオブジェクト指向プログラミングよりもずっと一般的な意味を持ちます。 
  
オブジェクト識別子の構文とサンプル オブジェクト識別子は、MAPIOID で定義されます。H ヘッダー ファイル。 値は **PR_ATTACH_TAG** MAPIOID.H で定義されている値に限定されません。 
  
これらのオブジェクト識別子の詳細については、ASN.1、X.208、X.209 のドキュメントを参照してください。 オブジェクト識別子は、ファイル転送本文パーツ (FTBP) 環境のアプリケーション参照要素に含まれる。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagAttachMimeTag 標準プロパティ](pidtagattachmimetag-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

