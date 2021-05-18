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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327966"
---
# <a name="pidtaganr-canonical-property"></a>PidTagAnr 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳コンテナーのコンテンツ テーブルのプロパティ制限で使用する文字列値が含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ANR、PR_ANR_A、PR_ANR_W  <br/> |
|識別子:  <br/> |0x360C  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、どのオブジェクトにも属していない。 [SPropertyRestriction](spropertyrestriction.md) 構造体のアドレス帳プロバイダーによって提供されます。 このプロパティには、アドレス帳コンテナーのコンテンツ テーブルに対してテストして、対応するメッセージ受信者を検索できるあいまいな名前解決 (ANR) 文字列が含まれます。 
  
アドレス帳プロバイダーは、プロバイダー定義の照合アルゴリズムPR_ANRを使用して、コンテンツ テーブル **内のすべての** エントリに対して、PR_ANRおよび関連付けられたプロパティの値と一致します。 この一致で使用される列は、アルゴリズムの一部としてプロバイダーによって選択されます。 **[PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 列が最も一般的に使用されます。**[PR_ACCOUNT** ] ([PidTagAccount](pidtagaccount-canonical-property.md)) 列は、ユーザーの電子メール名が含まれている場合にも便利です。 
  
あいまいな名前解決の詳細については、「アドレス帳の [制限」を参照してください](address-book-restrictions.md)。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

