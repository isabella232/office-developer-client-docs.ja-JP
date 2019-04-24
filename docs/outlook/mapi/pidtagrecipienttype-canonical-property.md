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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355259"
---
# <a name="pidtagrecipienttype-canonical-property"></a>PidTagRecipientType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ受信者の受信者の種類が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|識別子:  <br/> |0x0c15  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>解説

このプロパティに含まれる受信者の種類は、1つの必須値と1つの省略可能なフラグで構成されます。
  
このプロパティには、次のいずれかの値を含める必要があります。
  
MAPI_TO 
  
> 受信者がプライマリ受信者である。 クライアントは、プライマリ受信者を処理する必要があります。 その他の型はオプションです。
    
MAPI_CC 
  
> 受信者はカーボンコピー (cc) 受信者で、プライマリ受信者に加えてメッセージを受信する受信者です。
    
MAPI_BCC 
  
> 受信者がブラインドカーボンコピー (bcc) 受信者である。 プライマリおよびカーボンコピーの受信者は、BCC 受信者の存在を認識しません。 
    
MAPI_P1 
  
> 前回の試行で、受信者がメッセージを正常に受信できませんでした。 これは、以前の転送を再送信します。
    
また、次のフラグを設定することもできます。
  
MAPI_SUBMITTED 
  
> 受信者は既にメッセージを受信しているので、再度受信する必要はありません。 これは、以前の転送を再送信します。 このフラグは、 **MAPI_TO**、 **MAPI_CC**、および**MAPI_BCC**の値と共に設定されます。 
    
MAPI_P1 の値と**MAPI_SUBMITTED**フラグは、1つ以上の目的の受信者への配信不能のためにメッセージが再送信される場合に使用されます。 この再送信では、クライアントは、メッセージを再度必要とせず、受信者一覧に表示する必要があるすべての受信者に**MAPI_SUBMITTED**を設定します。 以前にメッセージを受信しなかったすべての受信者について、クライアントは元の受信者の**PR_RECIPIENT_TYPE**値を変更せずに、さらに元の値の代わりに MAPI_P1 を使用して受信者のコピーを送信します。 このコピーは、実際の配信前に破棄され、受信者を P1 エンベロープに強制して、その受信者への物理的な再送信を保証します。 MAPI_P1 の受信者の場合は、 **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを FALSE に設定します。
  
クライアントが再送信フォームを表示すると、MAPI_P1 の受信者のみが表示されます。 ユーザーが追加の受信者を入力しない限り、メッセージが配信されると、メッセージが初めて送信されたときとまったく同じように受信者一覧が表示されます。 
  
**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))、および**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) の各プロパティは、受信者の種類に関連付けられています。 クライアントがメッセージの**imapiprop:: SaveChanges**を呼び出し、受信者の一覧に少なくとも1人の受信者がある場合、メッセージストアプロバイダーは次のようにこれらのプロパティを設定します。 
  
|**プロパティ**|**説明**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |1人以上の受信者が**MAPI_TO**受信者の場合は TRUE に設定します。  <br/> |
|PR_DISPLAY_CC  <br/> |1人以上の受信者が**MAPI_CC**受信者の場合は TRUE に設定します。  <br/> |
| PR_DISPLAY_BCC  <br/> |1人以上の受信者が**MAPI_BCC**受信者の場合は TRUE に設定します。  <br/> |
   
x. では、P1 または配信エンベロープは、受信者のアドレスのプロパティと、配信と返信を制御する任意のオプションフラグを含む、メッセージを配信するために必要な情報です。 P2 または表示エンベロープは、通常、メッセージテキスト自体以外の各受信者に表示される情報です。 通常、プライマリおよびコピーされた受信者名に加えて、件名、重要度、優先度、秘密度、および送信時刻が含まれます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagRecipientStatus 標準プロパティ](pidtagrecipientstatus-canonical-property.md)
  
[PidTagDisplayTo 標準プロパティ](pidtagdisplayto-canonical-property.md)
  
[PidTagDisplayBcc 標準プロパティ](pidtagdisplaybcc-canonical-property.md)
  
[PidTagDisplayCc 標準プロパティ](pidtagdisplaycc-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

