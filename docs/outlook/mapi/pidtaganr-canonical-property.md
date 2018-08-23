---
title: PidTagAnr 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cc5edf1c93ca94fb9d8cab302ccd8e96373cd94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581945"
---
# <a name="pidtaganr-canonical-property"></a>PidTagAnr 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
アドレス帳コンテナーのコンテンツ テーブルのプロパティ制限で使用するための文字列値が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ANR、PR_ANR_A、PR_ANR_W  <br/> |
|識別子:  <br/> |0x360C  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、すべてのオブジェクトには属していません。それが[SPropertyRestriction](spropertyrestriction.md)構造体のアドレス帳のプロバイダーによって提供されています。 このプロパティには、対応するメッセージの受信者を検索するのには、アドレス帳コンテナーのコンテンツ テーブルを比較するあいまいな名前解決 (ANR) の文字列が含まれています。 
  
アドレス帳プロバイダーは、プロバイダーで定義されている一致のアルゴリズムを使用して**PR_ANR**と、内容のテーブル内の全てのエントリに関連付けられたプロパティの値を一致させます。 アルゴリズムの一部として、プロバイダーによっては、この一致で使用されている列が選択されます。 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) の列が頻繁に使用されます。**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) の列は、ユーザーの電子メール名が含まれている場合にも便利です。 
  
あいまいな名前解決の詳細については、[アドレス帳の制限](address-book-restrictions.md)を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

