---
title: PidTagDefaultPostMessageClass の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 538cc7cdc6dcb281beead6d06ff8644c534ed569
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802648"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a>PidTagDefaultPostMessageClass の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
カスタム フォームのメッセージ クラスの名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DEF_POST_MSGCLASS  <br/> |
|識別子:  <br/> |0x36E5  <br/> |
|データを入力します。  <br/> |PT_STRING8  <br/> |
|領域:  <br/> |MAPI のコンテナー  <br/> |
   
## <a name="remarks"></a>備考

値がいずれかを指定する必要がある場合は、フォルダーでこのプロパティを設定すると、正確に、ベース メッセージ クラス (たとえば、"IPM.連絡先 [連絡先フォルダーまたは"IPM.予定] の予定表フォルダー)、または、ベース メッセージ クラス (たとえば、"IPM.Contact.MyContact」)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
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
