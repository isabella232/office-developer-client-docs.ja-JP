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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415055"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>PidTagReceiveFolderSettings 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアの受信フォルダー設定のテーブルが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|識別子:  <br/> |0x3415  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。 型のプロパティPT_OBJECT [IMAPIProp::GetProps メソッドでは正常に取得](imapiprop-getprops.md) できません。その内容にアクセスするには [、IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを使用して、識別子を持つインターフェイスを要求IID_IMAPITable。 サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合はオプションで報告できます。 
  
表の内容を取得するには、クライアント アプリケーションが [IMsgStore::GetReceiveFolderTable メソッドを呼び出す必要](imsgstore-getreceivefoldertable.md) があります。 詳細については、「受信フォルダー テーブル [」を参照してください](receive-folder-tables.md)。
  
このプロパティには、メッセージ ストアの受信フォルダーのマッピングのテーブルが含まれています。 この **プロパティで OpenProperty** を呼び出すのは、メッセージ ストアで **GetReceiveFolderTable** を呼び出すのと同じです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

