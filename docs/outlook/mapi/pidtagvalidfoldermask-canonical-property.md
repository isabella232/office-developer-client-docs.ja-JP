---
title: PidTagValidFolderMask 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d8f501d4692e1e4ef735355f723ad8201e8a001d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599257"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>PidTagValidFolderMask 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア内のフォルダーのエントリ識別子の有効性を示すフラグのビットマスクが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|識別子:  <br/> |0x35DF  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>注釈

ユーザーがフォルダーを削除した場合、またはメッセージ ストアが破損した場合、フォルダーのエントリ識別子が無効になる可能性があります。
  
ビットマスクには、次のフラグを 1 つ以上設定できます。 
  
FOLDER_COMMON_VIEWS_VALID 
  
> 共通ビュー フォルダーには、有効なエントリ識別子があります。 **「PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId)」を参照してください](pidtagcommonviewsentryid-canonical-property.md)。
    
FOLDER_FINDER_VALID 
  
> finder フォルダーには、有効なエントリ識別子があります。 詳細 **についてはPR_FINDER_ENTRYID** ([PidTagFinderEntryId ) を参照してください](pidtagfinderentryid-canonical-property.md)。 
    
FOLDER_IPM_INBOX_VALID 
  
> 対人メッセージ (IPM) 受信フォルダーには、有効なエントリ識別子があります。 [「IMsgStore::GetReceiveFolder」を参照してください](imsgstore-getreceivefolder.md)。 
    
FOLDER_IPM_OUTBOX_VALID 
  
> IPM 送信ボックス フォルダーには、有効なエントリ識別子があります。 **「PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId)」を参照してください](pidtagipmoutboxentryid-canonical-property.md)。 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> IPM 送信アイテム フォルダーには、有効なエントリ識別子があります。 **「PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)」を参照してください](pidtagipmsentmailentryid-canonical-property.md)。
    
FOLDER_IPM_SUBTREE_VALID 
  
> IPM フォルダー サブツリーには、有効なエントリ識別子があります。 **「PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId)」を参照してください](pidtagipmsubtreeentryid-canonical-property.md)。
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> IPM 削除済みアイテム フォルダーには、有効なエントリ識別子があります。 **「PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)」を参照してください](pidtagipmwastebasketentryid-canonical-property.md)。
    
FOLDER_VIEWS_VALID 
  
> views フォルダーには、有効なエントリ識別子があります。 詳細 **についてはPR_VIEWS_ENTRYID** ([PidTagViewsEntryId ) を参照してください](pidtagviewsentryid-canonical-property.md)。
    
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

