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
ms.openlocfilehash: 3ddde5d206eb4be56ce6a7bae77eb00237f12a0f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584297"
---
# <a name="pidtagrecipienttype-canonical-property"></a>PidTagRecipientType 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージの受信者の受信者の種類が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|識別子:  <br/> |0x0C15  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティに格納されている受信者の種類は、1 つの必要な値と省略可能なフラグの 1 つで構成されます。
  
このプロパティは、次の値の 1 つだけを含める必要があります。
  
MAPI_TO 
  
> 受信者は、(受信者宛先) プライマリです。 クライアントは、プライマリ受信者を処理する必要があります。 その他のすべての種類は、オプションです。
    
MAPI_CC 
  
> 受信者は、主要な受信者だけでなくメッセージを受信する受信者、カーボン コピー (CC) 受信者です。
    
MAPI_BCC 
  
> 受信者は、ブラインド カーボン コピー (BCC) 宛先です。 プライマリおよびカーボン コピーの受信者は、BCC 受信者の存在を認識ではありません。 
    
MAPI_P1 
  
> 受信者は、以前の試行でメッセージを正常に受信しませんでした。 これは、以前に送信の再送信です。
    
さらに、次のフラグを設定できます。
  
MAPI_SUBMITTED 
  
> 受信者はメッセージを受信済みと、それを再度受信する必要はありません。 これは、以前に送信の再送信です。 **MAPI_TO**、 **MAPI_CC**、および**MAPI_BCC**の値と組み合わせて、このフラグが設定されています。 
    
MAPI_P1 値は、 **MAPI_SUBMITTED**フラグは、メッセージが 1 つまたは複数の受信者に配信不能が発生したため再送信されている場合に使用されます。 この再送信のためは、クライアントは、各受信者にメッセージを再度必要はありませんが、受信者の一覧に表示するかの**MAPI_SUBMITTED**を設定します。 以前のメッセージを受信しなかった受信者ごとに、クライアントとその**PR_RECIPIENT_TYPE**値を変更せずに、元の受信者が保持されますが、さらに、受信者は、元の値の代わりに MAPI_P1 でのコピーを送信します。 このコピーは、実際に配信する前に破棄すると、P1 封筒に受信者を強制的に、その受信者に物理的な再転送を保証 **れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) のプロパティは、MAPI_P1 の受信者の FALSE に設定されています。
  
クライアントには、再送信フォームが表示されたら、MAPI_P1 の受信者のみが表示されます。 メッセージが配信されると、追加の受信者を入力すると、しない限り、受信者の一覧には、最初にメッセージが送信されたときとまったく同じ状態が表示されます。 
  
**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) と**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) のプロパティは、受信者の種類に関連付けられます。 クライアントがメッセージの**IMAPIProp::SaveChanges**を呼び出すし、受信者の一覧に少なくとも 1 人の受信者が、メッセージ ストア プロバイダーはこれらのプロパティを次のように設定します。 
  
|**プロパティ**|**説明**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |**MAPI_TO**の受信者の 1 つ以上の受信者の場合は、TRUE に設定します。  <br/> |
|PR_DISPLAY_CC  <br/> |**MAPI_CC**の受信者の 1 つ以上の受信者の場合は、TRUE に設定します。  <br/> |
| PR_DISPLAY_BCC  <br/> |**MAPI_BCC**の受信者の 1 つ以上の受信者の場合は、TRUE に設定します。  <br/> |
   
X.400 は、P1 または配送の封筒は、受信者のアドレスのプロパティおよび配信し、応答を制御するオプション フラグのいずれかを含む、メッセージを配信するために必要な情報です。 P2 または表示の封筒は、メッセージ テキスト自体以外には、各受信者に通常表示される情報です。 通常、件名、重要度、優先度、感度、送信時刻とプライマリおよびコピーの受信者の名前を掲載しています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagRecipientStatus 標準プロパティ](pidtagrecipientstatus-canonical-property.md)
  
[PidTagDisplayTo 標準プロパティ](pidtagdisplayto-canonical-property.md)
  
[PidTagDisplayBcc 標準プロパティ](pidtagdisplaybcc-canonical-property.md)
  
[PidTagDisplayCc 標準プロパティ](pidtagdisplaycc-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

