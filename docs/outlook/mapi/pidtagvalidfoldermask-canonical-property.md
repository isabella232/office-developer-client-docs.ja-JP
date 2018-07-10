---
title: PidTagValidFolderMask の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ae09723c78fe4e333fb5c46e8c79da4b77c0b331
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803666"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>PidTagValidFolderMask の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ ストア内のフォルダーのエントリ id の有効性を示すフラグのビットマスクを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|識別子:  <br/> |0x35DF  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>備考

メッセージ ストアが破損した場合や、ユーザーがフォルダーを削除した場合フォルダーのエントリ id が無効になることができます。
  
1 つ以上次のフラグのビットマスクを設定できます。 
  
FOLDER_COMMON_VIEWS_VALID 
  
> 共通ビュー] フォルダーには、有効なエントリの識別子があります。 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) を参照してください。
    
FOLDER_FINDER_VALID 
  
> Finder フォルダーには、有効なエントリの識別子があります。 **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) を参照してください。 
    
FOLDER_IPM_INBOX_VALID 
  
> 個人間メッセージ (IPM) が表示されるフォルダーには、エントリの有効な識別子が含まれています。 [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を参照してください。 
    
FOLDER_IPM_OUTBOX_VALID 
  
> IPM が送信トレイ フォルダーには、有効なエントリの識別子があります。 **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) を参照してください。 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> IPM の送信済みアイテム フォルダーには、有効なエントリの識別子があります。 **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) を参照してください。
    
FOLDER_IPM_SUBTREE_VALID 
  
> IPM フォルダーのサブツリーには、有効なエントリの識別子があります。 **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) を参照してください。
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> IPM の削除済みアイテム フォルダーには、有効なエントリの識別子があります。 **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) を参照してください。
    
FOLDER_VIEWS_VALID 
  
> Views フォルダーには、有効なエントリの識別子があります。 **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) を参照してください。
    
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
