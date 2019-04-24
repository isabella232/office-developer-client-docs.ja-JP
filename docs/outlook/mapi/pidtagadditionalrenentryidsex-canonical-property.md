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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335204"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>PidTagAdditionalRenEntryIdsEx 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
store オブジェクトの特別なフォルダーエントリ id が格納されています。 この複数値を持つプロパティの各エントリは、1つまたは複数のエントリ id にマップできます。つまり、エントリとそれに関連付けられたエントリ id との間に一対多の関係があります。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|識別子:  <br/> |0x36D9  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>解説

このプロパティを使用すると、フォルダーのエントリ id を指定するブロックの配列が含まれます。 ブロックは、次の4つの表で指定された形式に従います。
  
**persistdata ブロック**

|**名前**|**Type**|**Size**|**説明**|
|:-----|:-----|:-----|:-----|
|**persistid** <br/> |WORD  <br/> |pbm-2  <br/> |この**persistdata**エントリの型識別子の値。 有効な値の一覧については、「persistblocktype Values」テーブルを参照してください。  <br/> |
|**data要素サイズ** <br/> |WORD  <br/> |pbm-2  <br/> |**dataelements**フィールドのサイズ (バイト単位)。  <br/> |
|**dataelements** <br/> |**persistelement**ブロックの配列  <br/> |変数  <br/> |ストアに存在する**persistelement**エントリの数を示します。 この構造体の形式については、「persistelement Block」の表を参照してください。  <br/> |
   
**persistblocktype の値**

|**Name**|**値**|**説明**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |これ以上の**persistdata**ブロックは処理されないことを示します。  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |このブロックには、RSS 購読フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |このブロックには、追跡対象メール処理フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |このブロックに、To do 検索フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |このブロックに、会話アクション設定フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |この値は予約されています。  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |このブロックには、推奨される連絡先フォルダーのデータが含まれていることを示します。  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |このブロックに、連絡先検索フォルダーのデータが含まれていることを示します。  <br/> Outlook でのみ使用されます。  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800a  <br/> |このブロックに、インスタントメッセージング (IM) 連絡先リストフォルダーのデータが含まれていることを示します。 参照フォルダーには、IM 連絡先リスト内の各グループを表す個人用配布リスト (pdls) が含まれています。  <br/> Outlook と Exchange の両方で使用されます。  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800b  <br/> |このブロックには、IM 連絡先フォルダーのデータが含まれていることを示します。 参照フォルダーには、IM 連絡先リストグループによって参照される個々の連絡先が含まれています。  <br/> Outlook と Exchange の両方で使用されます。  <br/> |
   
**persistblocktype**値がここで定義されていない場合、 **persistdata**ブロックは無視され、PERSIST_SENTINEL **persistid**が処理されるか、またはストリームの終わりに達するまで、処理は続行されます。 
  
**persistelementblock**

|**名前**|**Type**|**Size**|**説明**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |pbm-2  <br/> |この**persistelement**ブロックの型識別子の値を指定します。 有効な値の一覧については、「persistelementtype Values」テーブルを参照してください。  <br/> |
|**elementdatasize** <br/> |WORD  <br/> |pbm-2  <br/> |**elementdata**フィールドのサイズをバイト単位で指定します。  <br/> |
|**elementdata** <br/> |バイナリデータの配列  <br/> |変数  <br/> |この**persistid** + の**ElementID**ペアのデータを格納します。  <br/> |
   
**persistelementtype の値**

|**Name**|**Value**|**elementdatasize の値**|**説明**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |このブロックの**elementdata**フィールドに DWORD ヘッダーの値が含まれていることを示します。 この値がどのように解釈されるかは、ブロックの**persistid**型によって異なります。  <br/> [[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)で指定されているすべての**persistid**型の場合、この値は0です。  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |変数  <br/> |このブロックには、 **persistid**で指定されたフォルダーの**EntryID**が含まれていることを示します。  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |これ以上、 **persistelement**ブロックが処理されないことを示します。  <br/> |
   
**persistelementtype**の値がここで定義されている値ではない場合、 **persistelementtype**ブロックは無視され、ELEMENT_SENTINEL **ElementID**が処理されるか、またはストリームの終わりに達するまで、処理は続行されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。
    
[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。
    
[[OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> 受信者を漏洩機密情報 (パスワードやその他の個人情報など) に信頼できないソースに誘導するように設計された電子メールメッセージを識別してマークします。
    
### <a name="header-files"></a>ヘッダーファイル

Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

