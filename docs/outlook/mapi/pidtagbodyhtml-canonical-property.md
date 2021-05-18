---
title: PidTagBodyHtml 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359046"
---
# <a name="pidtagbodyhtml-canonical-property"></a>PidTagBodyHtml 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ テキストのハイパーテキスト マークアップ言語 (HTML) バージョンが含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_BODY_HTML、PR_BODY_HTML_A、PR_BODY_HTML_W  <br/> |
|識別子:  <br/> |0x1013  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティには、HTML 内の PR_BODY_CONTENT_LOCATION **(** [PidTagBodyContentLocation)](pidtagbodycontentlocation-canonical-property.md)と同じメッセージ テキストが含まれる。 
  
HTML をサポートするメッセージ ストアは、このフラグ [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)で STORE_HTML_OK **フラグをPR_STORE_SUPPORT_MASK** 示します。 
  
 **メモ** **STORE_HTML_OK** は、Microsoft 2000 Server 以前に含まれている Mapidefs.h のバージョン® Exchange定義されていません。 定義 **STORE_HTML_OK** 場合は、代わりに値0x00010000使用します。 
  
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

