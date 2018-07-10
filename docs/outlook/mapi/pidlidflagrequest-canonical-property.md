---
title: PidLidFlagRequest の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: df2e474206559dadf250bdf9a078c69da61187c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801974"
---
# <a name="pidlidflagrequest-canonical-property"></a>PidLidFlagRequest の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
会議出席依頼のステータスを表します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidRequest  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008530  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |フラグを設定します。  <br/> |
   
## <a name="remarks"></a>備考

Microsoft Office Outlook の会議出席依頼は予定アイテムです。
  
このプロパティは、フラグに関連付けられるユーザーを指定できるテキストが含まれていて、メッセージ オブジェクトのフラグを設定または完了すると、設定する必要がありますが、会議に関連するオブジェクトが存在する必要があります。 クライアントの選択せずに、このプロパティをサポートして、常に「フォロー アップ」(該当する場合、ユーザーの言語に翻訳された) を記述を使用する可能性がありますこのプロパティを設定する必要があるときに文字列の値とします。 このプロパティは、 **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) と**dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) のプロパティの値に基づいて条件付きで無視する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
