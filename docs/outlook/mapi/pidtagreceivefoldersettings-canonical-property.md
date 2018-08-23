---
title: PidTagReceiveFolderSettings 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c8bd8c7fb2ff5a030cd96e4c3ac2bbb4b6b16ce5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571459"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>PidTagReceiveFolderSettings 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージのテーブルが含まれているストアのフォルダーの設定を表示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|識別子:  <br/> |0x3415  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>注釈

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
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

