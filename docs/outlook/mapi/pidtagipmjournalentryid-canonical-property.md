---
title: PidTagIpmJournalEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmJournalEntryId
api_type:
- HeaderDef
ms.assetid: a3765b9d-a108-46d7-a97c-a825ae3980be
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b5dfc378a2558e906bec018608e2d2c776090c06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327910"
---
# <a name="pidtagipmjournalentryid-canonical-property"></a>PidTagIpmJournalEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[ジャーナル] フォルダーの **entryID** Outlookします。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IPM_JOURNAL_ENTRYID  <br/> |
|識別子:  <br/> |0x36D2  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、受信トレイ フォルダーとメッセージ ストアのルート フォルダーに格納されます。 特定のメッセージ ストアのプロパティにアクセスするには、次の操作を行います。 
  
1. 最初に、受信トレイ フォルダー内のプロパティを探します。 受信トレイ フォルダーの **EntryID** への参照を取得するには [、IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を使用します。 
    
2. **IMsgStore::GetReceiveFolder** が成功した場合は、受信トレイと [IMsgStore::OpenEntry](imsgstore-openentry.md)の **EntryID** への参照を使用して受信トレイを開き **、IMAPIFolder** オブジェクトへの参照を取得します。 
    
3. **IMsgStore::OpenEntry** が成功した場合は **、IMAPIFolder** オブジェクトと [IMAPIProp::GetProps](imapiprop-getprops.md)への返される参照を使用して、目的のプロパティを取得します。 
    
4. 手順 1、2、または 3 に失敗した場合は、ルート フォルダー内のプロパティを探します。 これを行うには **、IMsgStore::OpenEntry** を使用して **、lpEntryID** に NULL を指定して、メッセージ ストアのルート フォルダーを開き **、IMAPIFolder** オブジェクトへの参照を取得します。 
    
5. ルート フォルダーを開くが成功した場合は **、IMAPIFolder** オブジェクトと **IMAPIProp::GetProps** への返される参照を使用して、目的のプロパティを取得します。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。
    
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

