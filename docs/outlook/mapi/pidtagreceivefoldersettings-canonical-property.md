---
title: PidTagReceiveFolderSettings の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e93325873f1d9e89bb591d136df04aa27403375f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803278"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>PidTagReceiveFolderSettings の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージのテーブルが含まれているストアのフォルダーの設定を表示します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|識別子:  <br/> |0x3415  <br/> |
|データを入力します。  <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)操作で除外または[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作に含まれることができます。 PT_OBJECT の型のプロパティとして、正常に取得できません、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドで方式では[IMAPIProp::OpenProperty](imapiprop-openproperty.md) IID_IMAPITable の識別子を持つインターフェイスを要求するその内容にアクセスする必要があります。 サービス プロバイダーする必要がありますに報告して、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドが設定されているが報告したことができます (オプション)、または設定されていない場合はありません。 
  
テーブルの内容を取得するには、クライアント アプリケーションは、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドを呼び出す必要があります。 詳細については、[表示されるフォルダーのテーブル](receive-folder-tables.md)を参照してください。
  
このプロパティには、メッセージ ・ ストア用の受信フォルダーのマッピングのテーブルが含まれています。 このプロパティに**OpenProperty**を呼び出すことは、メッセージ ・ ストアに対して**GetReceiveFolderTable**を呼び出すことと同じです。 
  
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

