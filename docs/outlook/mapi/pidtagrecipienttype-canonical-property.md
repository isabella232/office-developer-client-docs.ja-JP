---
title: PidTagRecipientType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355259"
---
# <a name="pidtagrecipienttype-canonical-property"></a>PidTagRecipientType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ受信者の受信者の種類を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|識別子:  <br/> |0x0C15  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティに含まれる受信者の種類は、1 つの必須値と 1 つのオプション フラグで構成されます。
  
このプロパティには、次のいずれかの値が含まれている必要があります。
  
MAPI_TO 
  
> 受信者はプライマリ (宛先) 受信者です。 プライマリ受信者を処理するには、クライアントが必要です。 その他の型はすべてオプションです。
    
MAPI_CC 
  
> 受信者はカーボン コピー (CC) 受信者で、プライマリ受信者に加えてメッセージを受信する受信者です。
    
MAPI_BCC 
  
> 受信者はブラインド カーボン コピー (BCC) 受信者です。 プライマリ コピー受信者とカーボン コピー受信者は、BCC 受信者の存在を知らされません。 
    
MAPI_P1 
  
> 受信者が前回の試行でメッセージを正常に受信しなかった。 これは、以前の送信の再送信です。
    
さらに、次のフラグを設定できます。
  
MAPI_SUBMITTED 
  
> 受信者は既にメッセージを受信済みで、もう一度受信する必要はありません。 これは、以前の送信の再送信です。 このフラグは、パラメーター値、MAPI_TO **値**、MAPI_CC **値MAPI_BCC****されます。** 
    
メッセージMAPI_P1値と MAPI_SUBMITTED フラグは、意図した受信者の **1** つ以上への配信が不必要な理由でメッセージが再送信される場合に使用されます。 この再送信では、MAPI_SUBMITTEDメッセージを必要としませんが、受信者リストに表示する必要があるすべての受信者に対してクライアント が設定されます。 以前にメッセージを受信しなかったすべての受信者に対して、クライアントは元の受信者 **の PR_RECIPIENT_TYPE** 値を変更されずに保持しますが、さらに、元の値の代り MAPI_P1 を持つ受信者のコピーを送信します。 このコピーは、実際の配信前に破棄され、受信者が強制的に P1 エンベロープに入り、その受信者への物理的な再送信を保証します。 受信者 **PR_RESPONSIBILITY** に対して、プロパティ [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)プロパティが FALSE にMAPI_P1されます。
  
クライアントが再送信フォームを表示すると、受信者MAPI_P1表示されます。 ユーザーが追加の受信者を入力しない限り、メッセージの配信時に、メッセージが初めて送信された場合とまったく同じ受信者リストが表示されます。 
  
PR_DISPLAY_TO  ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) **、PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) プロパティ、**および PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) プロパティは、受信者の種類に関連しています。 クライアントがメッセージの **IMAPIProp::SaveChanges** を呼び出し、受信者リストに少なくとも 1 人の受信者がある場合、メッセージ ストア プロバイダーは次のようにこれらのプロパティを設定します。 
  
|**Property**|**説明**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |1 つ以上の受信者が受信者にアクセスしている場合は **、true に設定** MAPI_TOします。  <br/> |
|PR_DISPLAY_CC  <br/> |受信者の 1 つ以上が受信者の場合は **true にMAPI_CC** します。  <br/> |
| PR_DISPLAY_BCC  <br/> |1 つ以上の受信者が受信者の場合は **true にMAPI_BCC** します。  <br/> |
   
X.400 では、P1 または配信エンベロープは、受信者のアドレス プロパティや配信と返信を制御するオプション フラグなど、メッセージの配信に必要な情報です。 P2 または表示封筒は、通常、メッセージ テキスト自体以外の各受信者に表示される情報です。 通常、件名、重要度、優先度、感度、提出時間、プライマリおよびコピーされた受信者名が含まれます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagRecipientStatus 標準プロパティ](pidtagrecipientstatus-canonical-property.md)
  
[PidTagDisplayTo 標準プロパティ](pidtagdisplayto-canonical-property.md)
  
[PidTagDisplayBcc 標準プロパティ](pidtagdisplaybcc-canonical-property.md)
  
[PidTagDisplayCc 標準プロパティ](pidtagdisplaycc-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

