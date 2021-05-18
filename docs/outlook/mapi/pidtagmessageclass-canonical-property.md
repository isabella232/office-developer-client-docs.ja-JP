---
title: PidTagMessageClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359265"
---
# <a name="pidtagmessageclass-canonical-property"></a>PidTagMessageClass 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
IPM.Note など、送信者が定義したメッセージ クラスを識別するテキスト文字列が含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_CLASS、PR_MESSAGE_CLASS_A、PR_MESSAGE_CLASS_W  <br/> |
|識別子:  <br/> |0x001A  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |共通  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ クラスは、メッセージの種類を指定します。 メッセージに対して定義されたプロパティのセット、メッセージが伝える情報の種類、およびメッセージの処理方法を決定します。 
  
これらのプロパティには、ピリオドと連結された文字列が含まれます。 各文字列は、サブクラス化のレベルを表します。 たとえば、IPM です。メモは IPM のサブクラスであり、IPM のスーパークラスです。Note.Private。 
  
これらのプロパティは、ASCII 文字 32 ~ 127 で構成する必要があります。ピリオド (ASCII 46) で終わることはできません。 並べ替えと比較の操作では、大文字と小文字を区別しない文字列として扱う必要があります。 指定できる最大長は 255 文字ですが、MAPI ルームで修飾子を追加するには、元の長さを 128 文字以内に保つ必要があります。 
  
これらのプロパティを指定するには、すべてのメッセージが必要です。 通常、新しいメッセージを作成するクライアント アプリケーションは [、IMAPIFolder::CreateMessage](imapifolder-createmessage.md) が正常に返されるとすぐに設定します。 ただし、クライアントが [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出す際にプロパティが設定されていない場合は、メッセージ ストアで IPM に設定する必要があります。 
  
MAPI によって定義される値は次のとおりです。 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM と IPC はスーパークラスのみを対象とします。メッセージには、保存または送信の前に少なくとも 1 つのサブクラス修飾子が追加されている必要があります。 メッセージ クラスの使用方法の詳細については、「Message [Classes」を参照してください](mapi-message-classes.md)。 メッセージ クラスの必須プロパティとオプション プロパティの一覧については、「メッセージプロパティについて」のサブ [トピックを参照してください](message-properties-overview.md)。
  
カスタム メッセージ クラスは、そのメッセージ クラスでのみ使用するために予約範囲のプロパティを定義できます。 詳細については、「プロパティ識別子 [について」を参照してください](mapi-property-identifier-overview.md)。 
  
メッセージ クラスは、受信メッセージが格納されている受信フォルダーを制御します。 詳細については [、「IMsgStore::GetReceiveFolderTable メソッド」を参照](imsgstore-getreceivefoldertable.md) してください。 
  
フォームおよびフォーム サーバーでメッセージ クラスを使用する方法の詳細については、「メッセージ クラスの選択 [」を参照してください](choosing-a-message-class.md)。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> ボイス メールおよび FAX メッセージを表す場合に許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

