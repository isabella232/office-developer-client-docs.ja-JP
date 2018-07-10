---
title: PidTagMemberEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3139f7cc60d19048fb17c64101f279ce377e9b26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802977"
---
# <a name="pidtagmemberentryid-canonical-property"></a>PidTagMemberEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
システム アクセス制御リスト (SACL) テーブルのメンバーのディレクトリ オブジェクトのエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_MEMBER_ENTRYID  <br/> |
|識別子:  <br/> |0x0FFF  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>備考

[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスはこのプロパティを使用して、人や、SACL が適用されるロールを一意に識別します。 SACL の表に、メンバーが作成されると、**エントリ ID**は変更できません。 それを変更するには、テーブルのメンバーを削除し、別の**エントリ ID**で再作成する必要があります。
  
## <a name="related-resources"></a>関連リソース

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
