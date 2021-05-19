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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339355"
---
# <a name="pidtagsubmitflags-canonical-property"></a>PidTagSubmitFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの送信に関する詳細を示すフラグのビットマスクが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|識別子:  <br/> |0x0E14  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

次のフラグの 1 つ以上を、ビットマスクに **PR_SUBMIT_FLAGS** できます。 
  
SUBMITFLAG_LOCKED 
  
> MAPI スプーラーは現在、メッセージがロックされています。 
    
SUBMITFLAG_PREPROCESS 
  
> メッセージには前処理が必要です。 MAPI スプーラーは、このメッセージの前処理が完了したら [、IMessage::SubmitMessage メソッドを呼び出す必要](imessage-submitmessage.md) があります。 メッセージ ストア プロバイダーは、スプーラーがクライアント アプリケーションではなく **SubmitMessage** を呼び出し、フラグをクリアし、メッセージの送信を続行することを認識します。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

