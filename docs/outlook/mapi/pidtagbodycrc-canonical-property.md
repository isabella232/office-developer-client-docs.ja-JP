---
title: PidTagBodyCrc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415181"
---
# <a name="pidtagbodycrc-canonical-property"></a>PidTagBodyCrc 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ テキストの循環冗長チェック (CRC) 値を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_BODY_CRC  <br/> |
|識別子:  <br/> |0x0E1C  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ストアでは、値を生成する任意の CRC アルゴリズムPT_LONGできます。 PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)) プロパティが初めて設定され、その後変更されるたびに、**この** プロパティを [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの一部として計算する必要があります。
  
クライアント アプリケーションは **、PR_BODY_CRC** プロパティまたはバリアントに含まれるメッセージ テキスト文字列を比較 **PR_BODY使用します** 。 このプロパティを使用すると、クライアントはメッセージ テキストが変更された時点を迅速かつ簡単に検出できます。 メッセージ ストアから PR_BODY_CRC を取得しPR_BODYバージョンと比較する代わりに、パフォーマンスの大幅な向上を実現できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

