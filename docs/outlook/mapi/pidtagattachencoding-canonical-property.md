---
title: PidTagAttachEncoding 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345494"
---
# <a name="pidtagattachencoding-canonical-property"></a>PidTagAttachEncoding 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルのエンコーディングを指定する、ASN を含むオブジェクト識別子を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_ENCODING  <br/> |
|識別子:  <br/> |0x3702  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、添付ファイル内のデータの変換に使用されるアルゴリズムを識別します。
  
 **メモ****PR_ATTACH_ENCODING**プロパティと**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) プロパティを混同しないようにしてください。 ペアになっていないか、関連付けられていません。 **PR_ATTACH_TAG**は、添付ファイルを最初に生成したアプリケーションを識別します。 "object" は、用語オブジェクトの識別子、およびオブジェクト指向プログラミングの場合よりも、X でより一般的な意味を持ちます。 
  
オブジェクト識別子の構文とサンプルオブジェクトの識別子は、MAPIOID で定義されています。H ヘッダーファイル。 **PR_ATTACH_ENCODING**の値は、MAPIOID で定義されている値に限定されません。H. たとえば、添付 Macintosh ファイルでは、MacBinary などの識別子を使用できます。 
  
これらのオブジェクト識別子の詳細については、209個のドキュメントを参照してください。 オブジェクト識別子は、ftbp (ファイル転送本文パーツ) 環境のアプリケーション参照要素にあります。 
  
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



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

