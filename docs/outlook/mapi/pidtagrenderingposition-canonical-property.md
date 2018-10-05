---
title: PidTagRenderingPosition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396198"
---
# <a name="pidtagrenderingposition-canonical-property"></a>PidTagRenderingPosition 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メインのメッセージのテキスト内の添付ファイルのレンダリングに使用する文字数で、オフセットが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RENDERING_POSITION  <br/> |
|識別子:  <br/> |0x370B  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

指定されたオフセットが-1 (0 xffffffff) の場合、このプロパティを使用して、添付ファイルは表示されません。 -1 以外のすべての値は、添付ファイルを表示するには ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティ内の位置を示します。
  
 **メモ**この**PR_BODY**プロパティで指定した文字は、添付ファイルに置き換えられます。 通常この文字がスペース、特別なプレース ホルダー文字を使用することもできます。 
  
このプロパティは、文字で表されます。 一部の文字セットでこれはバイトに相当します。 Unicode アプリケーションには、2 バイト文字の位置を計算できます。 2 バイト文字セット (DBCS) アプリケーションでは、1 文字につき 1 つと 2 つのバイトの間でそれらの文字の表現が異なるために、このプロパティの値までのテキストをスキャンする必要があります。
  
テキストをリッチ テキスト形式 (RTF) で、このプロパティを使用しない必要があります。 オブジェクトの添付ファイルのプレース ホルダーと呼ばれるエスケープ シーケンスで rtf 形式の描画位置が示されます。 このシーケンスは、文字列で構成されています`\objattph`通常、スペース、添付ファイルのレンダリングによって置き換えられる、1 つの文字の後にします。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
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

