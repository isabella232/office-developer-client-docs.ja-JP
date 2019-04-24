---
title: PidTagSubmitFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339355"
---
# <a name="pidtagsubmitflags-canonical-property"></a>PidTagSubmitFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ送信に関する詳細を示すフラグのビットマスクを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|識別子:  <br/> |0x0e14  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI ノンノンアウトテーブル  <br/> |
   
## <a name="remarks"></a>解説

**PR_SUBMIT_FLAGS**ビットマスクには、次の1つ以上のフラグを設定できます。 
  
SUBMITFLAG_LOCKED 
  
> MAPI スプーラーには、現在メッセージがロックされています。 
    
SUBMITFLAG_PREPROCESS 
  
> メッセージに前処理が必要です。 MAPI スプーラーがこのメッセージの前処理を完了すると、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出す必要があります。 メッセージストアプロバイダーは、クライアントアプリケーションではなく、スプーラーが**submitmessage**を呼び出し、フラグをクリアし、メッセージ送信を続行することを認識します。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

