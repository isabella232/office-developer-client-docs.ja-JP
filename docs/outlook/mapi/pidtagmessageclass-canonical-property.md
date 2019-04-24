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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359265"
---
# <a name="pidtagmessageclass-canonical-property"></a>PidTagMessageClass 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信者が定義したメッセージクラス (IPM など) を識別するテキスト文字列を格納します。こと. 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_CLASS、PR_MESSAGE_CLASS_A、PR_MESSAGE_CLASS_W  <br/> |
|識別子:  <br/> |0x001a  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |共通  <br/> |
   
## <a name="remarks"></a>解説

message クラスは、メッセージの種類を指定します。 メッセージに対して定義されているプロパティのセット、メッセージによって伝達される情報の種類、およびメッセージの処理方法を決定します。 
  
これらのプロパティには、ピリオドで連結された文字列が含まれています。 各文字列は、サブクラス化のレベルを表します。 たとえば、IPM.メモは、ipm のサブクラスであり、ipm のスーパークラスです。注プライベート。 
  
これらのプロパティは、32 ~ 127 の ascii 文字で構成する必要があり、末尾にピリオド (ASCII 46) を指定することはできません。 並べ替えおよび比較操作では、大文字と小文字を区別しない文字列として扱う必要があります。 可能な最大長は255文字ですが、MAPI ルームが修飾子を追加できるようにするには、元の長さを128文字の下に保持することをお勧めします。 
  
これらのプロパティを指定するには、すべてのメッセージが必要です。 通常、新しいメッセージを作成するクライアントアプリケーションは、 [imapifolder:: CreateMessage](imapifolder-createmessage.md)が正常に終了したことを設定します。 しかし、クライアントが[imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出すときに、プロパティが設定されていない場合は、メッセージストアが IPM に設定する必要があります。 
  
MAPI で定義されている値は次のとおりです。 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM および IPC はスーパークラスのみを対象としています。メッセージには、保存または送信する前に、少なくとも1つのサブクラス修飾子を追加する必要があります。 メッセージクラスの使用法の詳細については、「[メッセージクラス](mapi-message-classes.md)」を参照してください。 メッセージクラスの必須およびオプションのプロパティの一覧については、「[メッセージプロパティについて](message-properties-overview.md)」のサブトピックを参照してください。
  
カスタムメッセージクラスでは、そのメッセージクラスで使用するために、予約された範囲内のプロパティを定義できます。 詳細については、「[プロパティ識別子につい](mapi-property-identifier-overview.md)て」を参照してください。 
  
メッセージクラスは、受信メッセージが格納される受信フォルダーを制御します。 詳細については、 [IMsgStore:: getreceivefoldertable](imsgstore-getreceivefoldertable.md)メソッドを参照してください。 
  
フォームおよびフォームサーバーでのメッセージクラスの使用の詳細については、「[メッセージクラスを選択する](choosing-a-message-class.md)」を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
[[OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> ボイスメールおよび fax メッセージを表すために許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

