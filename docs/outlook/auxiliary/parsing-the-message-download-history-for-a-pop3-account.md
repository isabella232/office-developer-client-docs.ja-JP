---
title: POP3 アカウントのメッセージ ダウンロード履歴の解析
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: このトピックでは、ダウンロードまたはそのアカウントの削除されたメッセージを特定するのには、POP3 アカウントのメッセージのダウンロードの履歴を表す POP3 の BLOB の構造について説明します。
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389009"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>POP3 アカウントのメッセージ ダウンロード履歴の解析

このトピックでは、ダウンロードまたはそのアカウントの削除されたメッセージを特定するのには、POP3 アカウントのメッセージのダウンロードの履歴を表す POP3 の BLOB の構造について説明します。

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>メッセージのダウンロードの履歴を解析する理由

Outlook の Post Office プロトコル (POP) プロバイダーを取得し、ローカル デバイス上の新しい電子メール メッセージをダウンロードしてその後に残すかメール サーバー上のこれらの電子メール メッセージを削除できます。 メール クライアントは、ダウンロードする新しいメッセージをチェックし、識別し、その受信トレイの新着メッセージのみをダウンロードできるようにする必要があります。 メール クライアントは、一意の識別子 (UID)、その受信トレイに配信されたことをメッセージごとのマップを入手するのには (一意な ID を一覧表示) UIDL コマンドを使用します。 クライアントは、ダウンロードまたはそのクライアントの受信トレイで削除されたメッセージのメッセージのダウンロードの履歴を取得します。 メッセージ マップの UID とダウンロードの履歴を使用して、クライアントことができますし、メッセージを識別するそれらは存在しない新規となり、履歴からをダウンロードする必要があります。
  
受信トレイのメッセージ ダウンロードの履歴を取得します。
  
- POP3 アカウントのメッセージの履歴を表すバイナリ ラージ オブジェクト (BLOB) が含まれています、 [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティを検索するのには[、POP3 アカウントの履歴をダウンロードするメッセージを検索する](locating-the-message-download-history-for-a-pop3-account.md)に手順を実行します。 
    
- 、BLOB の構造を説明し、BLOB をダウンロードまたは POP3 アカウントの受信トレイで削除されたメッセージを識別する例を示していますが、このトピックを参照してください。

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>POP の BLOB の構造

POP BLOB 構造では、表 1 で説明したようは、**バージョン**および**カウント****カウント**数が null で終わるのでは、リソースのタグの後に、2 つのフィールドで始まります。 
  
**表 1 です。メッセージを表すバイナリ ラージ オブジェクトの構造は、POP3 アカウントの履歴をダウンロードします。**

|**BLOB のフィールド**|**Size**|**説明**|
|:-----|:-----|:-----|
|**Version** <br/> |2 バイト  <br/> |3 (**PBLOB_VERSION_NUM**) をする必要があります。  <br/> |
|**Count** <br/> |2 バイト  <br/> |リソースの数は、この BLOB にタグ付けします。  <br/> |
|リソース タグ  <br/> |変数  <br/> |リソース タグのエンコードが UTF-8 文字列を 0 または null で終わる。 Null で終わる文字列の数は、**カウント**をと一致する必要があります。  <br/> |
   
各リソースのタグは、メッセージ、操作に関するいくつかの日付と時刻のメタデータに適用され、メッセージの UID をエンコードする操作を指定します。 リソース タグ文字列の形式は次のように分割して表 2 の詳細については。 
  
`Ocyyyymmddhhmmssuuu...`
  
**表 2 になります。リソース タグの構造**

|**リソース タグ内のフィールド**|**Size**|**説明**|
|:-----|:-----|:-----|
| `O` <br/> |1 文字  <br/> |電子メール メッセージに対して操作を実行します。 値である必要があります「+」、"-"、または"&amp;"、成功の取得、削除、または取得および削除の操作をそれぞれ示します。  <br/> |
| `c` <br/> |1 文字  <br/> |操作に関連するメッセージの内容の一部です。 値である必要があります""、"h"または"b"は、「なし」内容を指定するには、ヘッダーや本文をそれぞれ。  <br/> |
| `yyyy` <br/> |4 文字  <br/> |操作の 4 桁の年。  <br/> |
| `MM` <br/> |2 文字  <br/> |操作の 2 桁の月です。  <br/> |
| `dd` <br/> |2 文字  <br/> |操作の 2 桁の日です。  <br/> |
| `hh` <br/> |2 文字  <br/> |操作の 2 桁の時間。  <br/> |
| `mm` <br/> |2 文字  <br/> |操作の 2 桁の分。  <br/> |
| `ss` <br/> |2 文字  <br/> |2 桁の 2 番目の操作です。  <br/> |
| `uuu…` <br/> |可変長  <br/> |エンコードされたメッセージの UID です。  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>例

図 1 では、POP アカウントのメッセージのダウンロードの履歴を表すバイナリ ラージ オブジェクトの例を示します。 
  
**図 1 です。メッセージの BLOB の構造の例は、POP3 アカウントの履歴をダウンロードします。**

![POP3 アカウントのメッセージ ダウンロード履歴の BLOB](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
表 1 と表 2 に記載されている構造に基づき、この BLOB は、23 の電子メール メッセージのダウンロードの履歴を表します。
  
生の UID で各リソースのタグを解析するには、このエンコーディングを UID が続くことに注意してください: UID の文字は、ほとんどの英数字、および各英数字以外の文字が前に、ASCII 文字「$」(0x24)。 ASCII 文字 $ 2 d は、英数字以外の文字を使用するように"-"です。 リソース タグ 1 で生の UID を対応する ASCII 文字に変換する最初の前に実際の UID を生成するには、「$」、英数字以外の文字に変換する例を図 2 に示します。
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**図 2 になります。リソース タグで生の UID を実際のメッセージの UID に変換します。**

![BLOB の生の UID から実際のメッセージ UID への変換](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
この BLOB のリソース タグ 1 を解釈する: メッセージの UID を持つ`0BC535DB-EA63-11E1-A75C-00215AD7BB74`13時 11分: 38 で、2012 年 9 月 6 日に正常に取得しました。 
  
22 リソースの残りのタグは、その BLOB を同様に解析できます。
  
## <a name="see-also"></a>関連項目
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)    
- [POP3 アカウントのメッセージのダウンロードの履歴を検索します。](locating-the-message-download-history-for-a-pop3-account.md)    
- [POP3 UIDL 履歴の解析](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

