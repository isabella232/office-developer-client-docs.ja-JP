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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355154"
---
# <a name="pidtagrenderingposition-canonical-property"></a>PidTagRenderingPosition 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メイン メッセージ テキスト内の添付ファイルのレンダリングに使用するオフセットを文字で含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RENDERING_POSITION  <br/> |
|識別子:  <br/> |0x370B  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

指定されたオフセットが -1 (0xFFFFFFFF) の場合、添付ファイルは、このプロパティを使用してレンダリングされません。 -1 以外のすべての値は、添付 **ファイルを** レンダリングする PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ内の位置を示します。
  
 **メモ** ファイル内のこのプロパティで示 **PR_BODY** は添付ファイルに置き換えられる。 通常、この文字はスペースですが、特別なプレースホルダー文字も使用できます。 
  
このプロパティは文字で表されます。 一部の文字セットでは、これはバイトと同等ではありません。 Unicode アプリケーションは、2 バイト文字に基づいて位置を計算できます。 Double-Byte文字セット (DBCS) アプリケーションは、文字表現が 1 文字あたり 1 バイトから 2 バイトの間で異なっているので、このプロパティ値までテキストをスキャンする必要があります。
  
このプロパティは、リッチ テキスト形式 (RTF) テキストと一緒に使用する必要があります。 レンダリング位置は、オブジェクト添付ファイルプレースホルダーと呼ばれるエスケープ シーケンスによって RTF で示されます。 このシーケンスは、文字列の後に単一の文字 (通常はスペース) が続き、添付ファイルのレンダリングに置き  `\objattph` 換えられる文字列で構成されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
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

