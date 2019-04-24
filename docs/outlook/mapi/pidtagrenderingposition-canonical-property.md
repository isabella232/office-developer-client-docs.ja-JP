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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355154"
---
# <a name="pidtagrenderingposition-canonical-property"></a>PidTagRenderingPosition 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メインメッセージテキスト内で添付ファイルをレンダリングするときに使用するオフセット (文字数) を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RENDERING_POSITION  <br/> |
|識別子:  <br/> |0x370b  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

指定したオフセットが-1 (0xffffffff) の場合、添付ファイルはこのプロパティを使用してレンダリングされません。 -1 以外のすべての値は、添付ファイルがレンダリングされる**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ内の位置を示します。
  
 **メモ****PR_BODY**でこのプロパティによって示される文字は、添付ファイルに置き換えられます。 通常、この文字はスペースですが、特別なプレースホルダー文字を使用することもできます。 
  
このプロパティは、文字で表されます。 一部の文字セットでは、これはバイト数と同じではありません。 Unicode アプリケーションは、2バイト文字に基づいて位置を計算できます。 2バイト文字セット (DBCS) アプリケーションがこのプロパティ値までテキストをスキャンする必要があるのは、文字ごとに1文字と2バイトの文字表現が異なるためです。
  
このプロパティは、リッチテキスト形式 (RTF) テキストには使用しないでください。 レンダリング位置は、RTF では、オブジェクトの添付ファイルプレースホルダーと呼ばれるエスケープシーケンスによって示されます。 このシーケンスは、文字列`\objattph`の後に1つの文字 (通常はスペース) で構成され、添付ファイルのレンダリングによって置き換えられます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
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

