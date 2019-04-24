---
title: PidTagContentUnreadCount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331872"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>PidTagContentUnreadCount 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアによって計算された、フォルダー内の未読メッセージ数を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTENT_UNREAD  <br/> |
|識別子:  <br/> |0x3603  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |フォルダー  <br/> |
   
## <a name="remarks"></a>解説

メッセージストアによって計算されたこのプロパティは、関連する2つの異なる目的で使用されます。 MAPI フォルダーオブジェクトには、フォルダー内のメッセージの数が含まれています。 カテゴリに分類された MAPI テーブルの見出し行には、その見出し行に対応するカテゴリの未開封の関連付けられていないメッセージの数が含まれます。
  
このプロパティには、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティで MSGFLAG_READ フラグが設定されていないフォルダーの内容のテーブル内のメッセージの数が含まれます。 **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) プロパティには、フォルダーのメッセージ数の合計が含まれています。 **PR_CONTENT_COUNT**およびこのプロパティは、クライアントに対しては値の取得のみ可能です。 
  
クライアントアプリケーションによっては、このプロパティの値に応じてカテゴリの見出し行が異なる場合があります。 たとえば、クライアントは、未読メッセージが太字になっているカテゴリを表示できます。 このプロパティをカテゴリとして使用することはできません。これを試行すると、 [IMAPITable:: sorttable](imapitable-sorttable.md)メソッドから MAPI_E_INVALID_PARAMETER 値が返されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
[[OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> コアテーブルオブジェクトの許容可能な操作が含まれています。
    
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

