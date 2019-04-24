---
title: POP3 アカウントのメッセージ ダウンロード履歴の解析
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: このトピックでは、pop3 アカウントのメッセージのダウンロード履歴を表す pop3 BLOB の構造について説明し、そのアカウントでダウンロードまたは削除されたメッセージを識別します。
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327766"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>POP3 アカウントのメッセージ ダウンロード履歴の解析

このトピックでは、pop3 アカウントのメッセージのダウンロード履歴を表す pop3 BLOB の構造について説明し、そのアカウントでダウンロードまたは削除されたメッセージを識別します。

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>メッセージのダウンロード履歴を解析する理由

Outlook の Post Office Protocol (POP) プロバイダーを使用すると、ユーザーは新しい電子メールメッセージをローカルデバイスで取得してダウンロードし、メールサーバー上でこれらの電子メールメッセージを残すか削除することができます。 メールクライアントは、新しいメッセージのダウンロードを確認するときに、その受信トレイの新しいメッセージのみを識別してダウンロードできる必要があります。 メールクライアントは、最初に UIDL (Unique ID リスト) コマンドを使用して、その受信トレイに配信された各メッセージのマップを一意の識別子 (UID) に取得します。 クライアントは、そのクライアント上で受信トレイに対してダウンロードまたは削除されたメッセージのメッセージダウンロード履歴も取得します。 メッセージ UID マップとダウンロード履歴を使用して、クライアントは、履歴に存在しないメッセージを新規として識別できるため、ダウンロードする必要があります。
  
受信トレイのメッセージダウンロード履歴を取得するには、次のようにします。
  
- pop3 アカウントのメッセージ[のダウンロード履歴](locating-the-message-download-history-for-a-pop3-account.md)を探す手順に従って、 [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティを検索します。このプロパティには、pop3 アカウントのメッセージ履歴を表すバイナリラージオブジェクト (BLOB) が含まれています。 
    
- このトピックでは、blob の構造について説明し、POP3 アカウントの受信トレイでダウンロードまたは削除されたメッセージを識別するための blob の例を示します。

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>POP BLOB 構造

表1で説明されているように、POP BLOB 構造は、**バージョン**と**数**の2つの**** フィールドで始まり、その後にリソースタグの数が続き、それぞれが null で終わります。 
  
**表1POP3 アカウントのメッセージダウンロード履歴を表す BLOB の構造**

|**BLOB のフィールド**|**Size**|**説明**|
|:-----|:-----|:-----|
|**バージョン** <br/> |2 バイト  <br/> |3 (**PBLOB_VERSION_NUM**) である必要があります。  <br/> |
|**Count** <br/> |2 バイト  <br/> |この BLOB 内のリソースタグの数。  <br/> |
|リソースタグ  <br/> |可変  <br/> |リソースタグをエンコードする0個以上の null で終了する utf-8 文字列。 null で終わる文字列の数は、 **Count**と一致する必要があります。  <br/> |
   
各リソースタグは、メッセージに適用される操作、操作に関する日付時メタデータ、およびメッセージの UID をエンコードします。 リソースタグ文字列の形式は、次のように分割されており、表2でさらに詳しく説明されています。 
  
`Ocyyyymmddhhmmssuuu...`
  
**表2リソースタグの構造**

|**リソースタグのフィールド**|**Size**|**説明**|
|:-----|:-----|:-----|
| `O` <br/> |1文字  <br/> |電子メールメッセージに対して実行された操作。 この値は、"+"、"-"、または&amp;"" のいずれかである必要があります。この値は、それぞれ、get、delete、または取得操作が正常に行われたことを示します。  <br/> |
| `c` <br/> |1文字  <br/> |操作に関係するメッセージコンテンツの一部。 値は、""、"h"、または "b" のいずれかである必要があります。この値は、それぞれ none、header、または body の内容を示します。  <br/> |
| `yyyy` <br/> |4文字  <br/> |操作の4桁の年。  <br/> |
| `MM` <br/> |2文字  <br/> |操作の2桁の月を示します。  <br/> |
| `dd` <br/> |2文字  <br/> |操作の2桁の日。  <br/> |
| `hh` <br/> |2文字  <br/> |操作の2桁の時間。  <br/> |
| `mm` <br/> |2文字  <br/> |操作の2桁の分。  <br/> |
| `ss` <br/> |2文字  <br/> |操作の2桁の秒。  <br/> |
| `uuu…` <br/> |可変長  <br/> |メッセージのエンコードされた UID。  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>例

図1は、POP アカウントのメッセージのダウンロード履歴を表す BLOB の例を示しています。 
  
**図1。POP3 アカウントのメッセージダウンロード履歴の BLOB 構造の例**

![POP3 アカウントのメッセージ ダウンロード履歴の BLOB](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
表1と表2に記載されている構造に基づいて、この BLOB は23件の電子メールメッセージのダウンロード履歴を表します。
  
各リソースタグの生の uid を解析するには、uid がこのエンコーディングに従っていることに注意してください。 uid 内の文字は大部分が英数字で、各英数字以外の文字の前には ASCII 文字の "$" (0x24) が付けられます。 そのため、ASCII 文字 $ 2d は英数字以外の文字 "-" を表します。 図2では、最初にリソースタグ1の生の UID を ASCII 表記に変換し、次に英数字以外の文字を "$" の前に変換して、実際の uid を生成する例を示します。
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**図2リソースタグ内の生の uid を実際のメッセージ uid に変換する**

![BLOB の生の UID から実際のメッセージ UID への変換](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
この BLOB 内のリソースタグ1を解釈するには、2012 `0BC535DB-EA63-11E1-A75C-00215AD7BB74`年9月6日に、UID を持つメッセージが13:11:38 に正常に取得されました。 
  
同様に、その BLOB の残りの22個のリソースタグを解析することもできます。
  
## <a name="see-also"></a>関連項目
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)    
- [POP3 アカウントのメッセージのダウンロードの履歴を検索します。](locating-the-message-download-history-for-a-pop3-account.md)    
- [POP3 の UIDL 履歴の解析](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

