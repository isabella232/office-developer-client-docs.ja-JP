---
title: POP3 アカウントのメッセージ ダウンロード履歴の解析
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: このトピックでは、そのアカウントでダウンロードまたは削除されたメッセージを識別するために、POP3 アカウントのメッセージダウンロード履歴を表す POP3 BLOB の構造について説明します。
ms.openlocfilehash: d9257c050fa7bd65922aa766b509b7cf0aa60615
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561867"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>POP3 アカウントのメッセージ ダウンロード履歴の解析

このトピックでは、そのアカウントでダウンロードまたは削除されたメッセージを識別するために、POP3 アカウントのメッセージダウンロード履歴を表す POP3 BLOB の構造について説明します。

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>メッセージのダウンロード履歴を解析する理由

Outlook の post Office プロトコル (POP) プロバイダーを使用すると、ユーザーはローカル デバイスで新しい電子メール メッセージを取得およびダウンロードし、その後、メール サーバー上でこれらの電子メール メッセージを残したり削除したりできます。 メール クライアントは、ダウンロードする新しいメッセージをチェックするときに、その受信トレイの新しいメッセージのみを識別してダウンロードできる必要があります。 メール クライアントは、まず UIDL (Unique ID Listing) コマンドを使用して、その受信トレイに一意の識別子 (UID) に配信された各メッセージのマップを取得します。 クライアントは、そのクライアントの受信トレイに対してダウンロードまたは削除されたメッセージのメッセージダウンロード履歴も取得します。 メッセージ UID マップとダウンロード履歴を使用して、クライアントは履歴から存在しないメッセージを新しいメッセージとして識別し、したがってダウンロードする必要があります。
  
受信トレイのメッセージダウンロード履歴を取得するには、次の方法を実行します。
  
- [「POP3](locating-the-message-download-history-for-a-pop3-account.md)アカウントのメッセージダウンロード履歴を検索する」の手順に従って、POP3 アカウントのメッセージ履歴を表すバイナリ ラージ オブジェクト (BLOB) を含む[PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティを検索します。 
    
- このトピックでは、BLOB の構造について説明し、POP3 アカウントの受信トレイに対してダウンロードまたは削除されたメッセージを識別するための BLOB の例を示します。

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>POP BLOB 構造

表 1 で説明されている POP BLOB 構造は、Versionと **Count** の 2つのフィールドから始まり、その後に Count のリソース タグの数が続き、それぞれが null で終了します。 
  
**表 1.POP3 アカウントのメッセージダウンロード履歴を表す BLOB の構造**

|**BLOB のフィールド**|**サイズ**|**説明**|
|:-----|:-----|:-----|
|**バージョン** <br/> |2 バイト  <br/> |3 ( PBLOB_VERSION_NUM )**である必要があります**。  <br/> |
|**Count** <br/> |2 バイト  <br/> |この BLOB 内のリソース タグの数。  <br/> |
|リソース タグ  <br/> |変数  <br/> |リソース タグをエンコードする 0 UTF-8 null 終端文字列。 null 終端文字列の数は Count と一致する **必要があります**。  <br/> |
   
各リソース タグは、メッセージに適用される操作、操作に関する日時のメタデータを指定し、メッセージの UID をエンコードします。 リソース タグ文字列の形式は次のように分解され、表 2 でさらに説明します。 
  
`Ocyyyymmddhhmmssuuu...`
  
**表 2.リソース タグの構造**

|**リソース タグのフィールド**|**サイズ**|**説明**|
|:-----|:-----|:-----|
| `O` <br/> |1 文字  <br/> |電子メール メッセージに対して実行された操作。 値は"+"、"-"、または ""である必要があります。これは、それぞれ正常な取得、削除、または &amp; get-and-delete 操作を示します。  <br/> |
| `c` <br/> |1 文字  <br/> |操作に関係するメッセージ コンテンツの部分。 値は"、"h"、または "b" である必要があります。これは、それぞれ none、ヘッダー、または本文の内容を示します。  <br/> |
| `yyyy` <br/> |4 文字  <br/> |操作の 4 桁の年。  <br/> |
| `MM` <br/> |2 文字  <br/> |操作の 2 桁の月。  <br/> |
| `dd` <br/> |2 文字  <br/> |操作の 2 桁の日。  <br/> |
| `hh` <br/> |2 文字  <br/> |操作の 2 桁の時間。  <br/> |
| `mm` <br/> |2 文字  <br/> |操作の 2 桁の分。  <br/> |
| `ss` <br/> |2 文字  <br/> |操作の 2 桁の秒。  <br/> |
| `uuu…` <br/> |可変長  <br/> |メッセージのエンコードされた UID。  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>例

図 1 は、POP アカウントのメッセージダウンロード履歴を表す BLOB の例を示しています。 
  
**図 1.POP3 アカウントのメッセージダウンロード履歴の BLOB 構造の例**

![POP3 アカウントのメッセージ ダウンロード履歴の BLOB](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
表 1 と表 2 に記載されている構造に基づいて、この BLOB は 23 の電子メール メッセージのダウンロード履歴を表します。
  
各リソース タグで生の UID を解析するには、UID は次のエンコードに従います。UID の文字は主に英数字で、英数字以外の各文字の前には ASCII 文字 "$" (0x24) が付きます。 したがって、ASCII 文字 $2d は英数字以外の文字 "-" を表します。 図 2 は、最初にリソース タグ 1 の生 UID を ASCII 表記に変換し、その後に"$" の前に英数字以外の文字を変換して実際の UID を生成する例を示しています。
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**図 2.リソース タグの生 UID を実際のメッセージ UID に変換する**

![BLOB の生の UID から実際のメッセージ UID への変換](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
この BLOB のリソース タグ 1 を解釈するには、UID を含むメッセージが  `0BC535DB-EA63-11E1-A75C-00215AD7BB74` 2012 年 9 月 6 日 13:11:38 に正常に取得されました。 
  
同様に、その BLOB の残りの 22 のリソース タグを解析できます。
  
## <a name="see-also"></a>関連項目
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)    
- [POP3 アカウントのメッセージのダウンロードの履歴を検索します。](locating-the-message-download-history-for-a-pop3-account.md)    
- [POP3 UIDL 履歴の解析](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

