---
title: PidTagAdditionalRenEntryIdsEx の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d3a8dc45bb131f5d2e7ff370617a10e3096a99f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802431"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>PidTagAdditionalRenEntryIdsEx の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ストア オブジェクトの特別なフォルダーのエントリ Id が含まれています。 この複数値プロパティ内の各エントリは、1 つまたは複数のエントリ Id にマップすることができます、つまり、エントリとその関連付けられたエントリ Id との間の一対多リレーションシップがあります。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|識別子:  <br/> |0x36D9  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>備考

このプロパティを使用する場合、フォルダーのエントリ Id を指定するブロックの配列が含まれています。 ブロックは、次の 4 つのテーブルで指定された形式に従います。
  
**ブロックのデータの保持**

|**名前**|**型**|**Size**|**説明**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |この**データの保持**のエントリの識別子の値を入力します。 有効な値の一覧については PersistBlockType 値」の表を参照してください。  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |**DataElements**フィールドのバイト単位のサイズです。  <br/> |
|**DataElements** <br/> |**PersistElement**ブロックの配列  <br/> |変数  <br/> |ストアの数の**PersistElement**エントリが存在することを示します。 この構造体の形式については「PersistElement ・ ブロック」表を参照してください。  <br/> |
   
**PersistBlockType 値**

|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |**データの保持**ブロックを処理することを示します。  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |このブロックに RSS 購読] フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |このブロックにメールの処理の履歴フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |このブロックに to do の検索フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |このブロックに、会話のアクションの設定] フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |この値は予約されています。  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |このブロックに提案された連絡先フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |このブロックに連絡先の検索フォルダーのデータが含まれていることを示します。  <br/> Outlook でのみ使用されます。  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |このブロックがインスタント メッセージング (IM) の連絡先リスト フォルダーのデータを格納することを示します。 個人用配布リスト (Pdl) IM の連絡先リストに含まれる各グループを表す、参照先のフォルダーが含まれます。  <br/> Outlook と Exchange の両方で使用されます。  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |このブロックに IM の連絡先フォルダーのデータが含まれていることを示します。 参照先のフォルダーには、IM の連絡先リストのグループによって参照される個々 の連絡先が含まれています。  <br/> Outlook と Exchange の両方で使用されます。  <br/> |
   
**PersistBlockType**の値がここで定義されているのいずれかでない場合は、**データの保持**のブロックは無視され、PERSIST_SENTINEL **PersistID**が処理されるか、ストリームの末尾に到達するまで処理は続行されます。 
  
**PersistElementBlock**

|**名前**|**型**|**Size**|**説明**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |**PersistElement**ブロックの型の識別子の値を指定します。 有効な値の一覧については PersistElementType 値」の表を参照してください。  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |**ElementData**フィールドのバイト単位のサイズを指定します。  <br/> |
|**ElementData** <br/> |バイナリ データの配列  <br/> |変数  <br/> |この**PersistID**のデータが含まれています + **ElementID**のペアです。  <br/> |
   
**PersistElementType 値**

|**名前**|**値**|**ElementDataSize の値**|**説明**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |**ElementData**フィールドこのブロックのにはヘッダーの DWORD 値が含まれていることを示します。 この値を解釈する方法は、ブロックの**PersistID**の種類によって異なります。  <br/> [[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)で指定されたすべての**PersistID**の種類、この値は 0 です。  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |変数  <br/> |このブロックに**PersistID**によって指定されたフォルダーの**エントリ Id**が含まれていることを示します。  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |**PersistElement**ブロックを処理することを示します。  <br/> |
   
**PersistElementType**の値がここで定義されているのいずれかでない場合は、 **PersistElement**ブロックは無視され、ELEMENT_SENTINEL の**ElementID**が処理されるか、ストリームの末尾に到達するまで処理は続行されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。
    
[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。
    
[[MS OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> 識別し、だまして受信者 (パスワードやその他の個人情報) などの機密情報を盗み、以外の信頼できる発行元に設計された電子メール メッセージをマークします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI Property Overview](mapi-property-overview.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

