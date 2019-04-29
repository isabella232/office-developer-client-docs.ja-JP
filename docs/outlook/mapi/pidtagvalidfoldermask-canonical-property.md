---
title: PidTagValidFolderMask 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427795"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>PidTagValidFolderMask 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストア内のフォルダーのエントリ識別子の有効性を示すフラグのビットマスクを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|識別子:  <br/> |0x35df  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI メッセージストア  <br/> |
   
## <a name="remarks"></a>注釈

ユーザーがフォルダーを削除したり、メッセージストアが破損したりすると、フォルダーのエントリ識別子が無効になることがあります。
  
ビットマスクには、次の1つ以上のフラグを設定できます。 
  
FOLDER_COMMON_VIEWS_VALID 
  
> common views フォルダーには、有効なエントリ識別子があります。 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) を参照してください。
    
FOLDER_FINDER_VALID 
  
> finder フォルダーには有効なエントリ識別子があります。 **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) を参照してください。 
    
FOLDER_IPM_INBOX_VALID 
  
> 個人間メッセージ (IPM) の受信フォルダーに有効なエントリ識別子があります。 [IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を参照してください。 
    
FOLDER_IPM_OUTBOX_VALID 
  
> IPM 送信トレイフォルダーに有効なエントリ識別子があります。 **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) を参照してください。 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> IPM 送信済みアイテムフォルダーには、有効なエントリ識別子があります。 **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) を参照してください。
    
FOLDER_IPM_SUBTREE_VALID 
  
> IPM フォルダーのサブツリーに有効なエントリ識別子がある。 **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) を参照してください。
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> IPM 削除済みアイテムフォルダーには、有効なエントリ識別子があります。 **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) を参照してください。
    
FOLDER_VIEWS_VALID 
  
> views フォルダーには有効なエントリ識別子があります。 **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) を参照してください。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

