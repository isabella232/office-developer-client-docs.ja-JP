---
title: PidTagJunkIncludeContacts の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4dde93bbec2594804ab18a3ee4eb3e116a57e528
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802914"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>PidTagJunkIncludeContacts の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
連絡先フォルダー内の連絡先の電子メール アドレスが迷惑メール フィルターについては特別に扱うかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|識別子:  <br/> |0x6100  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |スパム  <br/> |
   
## <a name="remarks"></a>備考

"0x00000001"に設定すると、これらの電子メール アドレスする必要がありますを先に設定、迷惑メール ルールの制限の「信頼された」の連絡先電子メール アドレスの部分をこれらのアドレスからのメールが「迷惑メール」として扱われます。 "0x00000000"に設定すると、連絡先フォルダーから電子メール アドレスする必要がありますに追加できません迷惑メールのルールとルールのセクションは NULL である必要があります。
  
このプロパティが"0x00000001"と追加した連絡先が迷惑メール ルールの「信頼されたアドレス帳にまだ含まれていない電子メール アドレスを持つ場合の値である場合制限これらの電子メール アドレスを追加しなければなりません。 このプロパティが"0x00000000"の場合は、操作する必要はありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
