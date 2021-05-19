---
title: PidTagAdditionalRenEntryIdsEx 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIdsEx
api_type:
- HeaderDef
ms.assetid: b5e896e7-c0c6-4ad1-bf91-9daba3a1e4d4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335204"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>PidTagAdditionalRenEntryIdsEx 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストア オブジェクトの特別なフォルダー エントリの ID を格納します。 この複数値プロパティの各エントリは、1 つ以上のエントリ ID にマップできます。つまり、エントリと関連するエントリ ID の間には 1 対多の関係があります。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|識別子:  <br/> |0x36D9  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Outlookアプリケーション  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティを使用する場合は、フォルダーのエントリの ID を指定するブロックの配列が含まれます。 ブロックは、次の 4 つの表で指定された形式に従います。
  
**PersistData ブロック**

|**名前**|**Type**|**[サイズ]**|**説明**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |この PersistData エントリの識別子 **の値を入力** します。 有効な値の一覧については、「PersistBlockType Values」テーブルを参照してください。  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |**DataElements** フィールドのサイズ (バイト単位)。  <br/> |
|**DataElements** <br/> |**PersistElement ブロックの** 配列  <br/> |変数  <br/> |ストアに存在 **する PersistElement** エントリの数を示します。 この構造の形式については、「PersistElement Block」テーブルを参照してください。  <br/> |
   
**PersistBlockType 値**

|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |PersistData ブロックが **処理され** なきを示します。  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |このブロックに RSS サブスクリプション フォルダーのデータが含まれているかどうかを示します。  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |このブロックに、追跡メール処理フォルダーのデータが含まれているかどうかを示します。  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |このブロックに、検索フォルダーのデータTo-Do示します。  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |このブロックに、スレッド アクション フォルダーのデータが含設定します。  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |この値は予約済みです。  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |このブロックに[推奨連絡先] フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |このブロックに連絡先検索フォルダーのデータが含まれているかどうかを示します。  <br/> ユーザーが使用するOutlook。  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |このブロックにインスタント メッセージング (IM) 連絡先リスト フォルダーのデータが含まれているかどうかを示します。 参照先のフォルダーには、IM 連絡先リスト内の各グループを表す個人用配布リスト (PDL) が含まれる。  <br/> この値は、OutlookとExchange。  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |このブロックに IM 連絡先フォルダーのデータが含まれているかどうかを示します。 参照先フォルダーには、IM 連絡先一覧グループによって参照される個々の連絡先が含まれる。  <br/> この値は、OutlookとExchange。  <br/> |
   
**PersistBlockType** 値がここで定義されている値の 1 つではない場合 **、PersistData** ブロックは無視され、PERSIST_SENTINEL **PersistID** が処理されるまで、またはストリームの末尾に達するまで処理が継続されます。 
  
**PersistElementBlock**

|**名前**|**Type**|**[サイズ]**|**説明**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |この PersistElement ブロックの型識別子 **の値を指定** します。 有効な値の一覧については、「PersistElementType Values」の表を参照してください。  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |ElementData フィールドのサイズをバイト単位 **で指定** します。  <br/> |
|**ElementData** <br/> |バイナリ データの配列  <br/> |変数  <br/> |この **PersistID ElementID ペアの**  +  **データを格納** します。  <br/> |
   
**PersistElementType 値**

|**名前**|**Value**|**ElementDataSize の値**|**説明**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |このブロックの **ElementData** フィールドに DWORD ヘッダー値が含まれているかどうかを示します。 この値の解釈方法は、ブロックの **PersistID 型によって異** なります。  <br/> [[MS-OXOSFLD] で](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)指定された **PersistID** 型の場合、この値は 0 です。  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |変数  <br/> |このブロックに **、PersistID** で指定されたフォルダーの **EntryID が含まれるかどうかを示します**。  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |**PersistElement** ブロックが処理されなきを示します。  <br/> |
   
**PersistElementType** 値がここで定義されている値の 1 つではない場合 **、PersistElement** ブロックは無視され、ELEMENT_SENTINEL **ElementID** が処理されるまで、またはストリームの末尾に達するまで処理が継続されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> 受信者を騙して機密情報 (パスワードや他の個人情報など) を信頼できないソースに開示するように設計された電子メール メッセージを識別およびマークします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

