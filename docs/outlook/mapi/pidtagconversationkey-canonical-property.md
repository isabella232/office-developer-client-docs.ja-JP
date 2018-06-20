---
title: PidTagConversationKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4aec52497e02e99423fa50f378cd35dbf366c37c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802633"
---
# <a name="pidtagconversationkey-canonical-property"></a>PidTagConversationKey の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
**IPM を検索するときにのみ、Microsoft Outlook で使用される対話鍵が含まれています。MessageManager** Post Office プロトコル (POP3) アカウントのダウンロードの履歴を格納しているメッセージなどのメッセージです。 Microsoft Exchange Server で、このプロパティは廃止されました。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONVERSATION_KEY  <br/> |
|識別子:  <br/> |0x000B  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

会話メッセージのプロパティを[トランスポート ニュートラル カプセル化形式 (TNEF)](transport-neutral-encapsulation-format-tnef.md)に変換すると電子メール メッセージにアクセスするときに、このプロパティを使用できません。代わりに、 [PidTagConversationIndex](pidtagconversationindex-canonical-property.md)および[PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)の標準的なプロパティを使用します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IPM サブツリー](ipm-subtree.md)
  
[MAPI の特別なフォルダーです。](mapi-special-folders.md)
  
[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

