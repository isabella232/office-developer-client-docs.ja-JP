---
title: PidTagRtfInSync 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 85e517601d291f144652befa267d8fd8f76dea64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803393"
---
# <a name="pidtagrtfinsync-canonical-property"></a>PidTagRtfInSync 標準プロパティ

  
  
**適用対象**: Outlook 
  
([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) である**PR_RTF_COMPRESSED**プロパティにこのメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のプロパティと同じテキストの内容がある場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RTF_IN_SYNC  <br/> |
|識別子:  <br/> |0x0E1F  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

値が ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティをこのメッセージのテキスト形式のバージョンと、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティをリッチ テキスト形式 (RTF) バージョンが同じ以外の場合は TRUE の場合**PR_BODY**と**PR_RTF_COMPRESSED**の書式設定に空白文字です。 2 つのバージョンのテキストは、同じ順序で同じ文字で構成されます。
  
FALSE は、2 つのバージョンがテキスト コンテンツは同期されません[へ](rtfsync.md)の関数によって同期されるの値です。 1 つのバージョンが変更されているし、他のバージョンには、ありません。 
  
値は、なし、2 つのバージョンでは、両方が存在か、以前存在していた場合は同期できません。 1 つのバージョンは削除されたり、大幅に同期が可能ではないことに変更します。
  
**PR_RTF_COMPRESSED**を変更したクライアント アプリケーションは、強制的に同期するには、このプロパティに false を指定の値を設定する必要があります。 RTF に対応してメッセージ ・ ストアには、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)の呼び出し中に**行う**を使用して、同期を実行します。 RTF に対応していないクライアントが**PR_RTF_COMPRESSED**を読む前に**PR_RTF_IN_SYNC**の設定を確認して必要な場合は最初の**行う**を呼び出します。 
  
**PR_BODY**が空白以外の値に変更がある場合、メッセージ ・ ストアは、同期を終了するのには**PR_RTF_IN_SYNC**を削除しなければなりません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
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

