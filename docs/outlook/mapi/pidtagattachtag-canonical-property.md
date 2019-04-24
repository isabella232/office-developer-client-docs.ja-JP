---
title: PidTagAttachTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361083"
---
# <a name="pidtagattachtag-canonical-property"></a>PidTagAttachTag 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルを提供したアプリケーションを指定する、ASN. 1 つのオブジェクト識別子を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_TAG  <br/> |
|識別子:  <br/> |0x370a  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、添付ファイルを最初に生成したアプリケーションを識別します。
  
 **メモ****PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) および**PR_ATTACH_TAG**プロパティは、混同しないようにしてください。 ペアになっていないか、関連付けられていません。 **PR_ATTACH_ENCODING**添付ファイル内のデータの変換に使用するアルゴリズムを指定します。 "object" は、用語オブジェクトの識別子、およびオブジェクト指向プログラミングの場合よりも、X の使用法でより一般的な意味を持ちます。 
  
オブジェクト識別子の構文とサンプルオブジェクトの識別子は、MAPIOID で定義されています。H ヘッダーファイル。 **PR_ATTACH_TAG**の値は、MAPIOID で定義されている値に限定されません。H. 
  
これらのオブジェクト識別子の詳細については、209個のドキュメントを参照してください。 オブジェクト識別子は、ファイル転送本文パーツ (ftbp) 環境のアプリケーション参照要素にあります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagAttachMimeTag 標準プロパティ](pidtagattachmimetag-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

