---
title: MAPI Url の通知に基づくインデックス作成について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 27ad80b9eca8332beeda147a8b2b4204f9f1cd38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799593"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>MAPI Url の通知に基づくインデックス作成について

**適用されます**: Outlook 
  
ストア プロバイダーには、オブジェクトのインデックス作成の準備が整っているインデクサーが通知された、MAPI プロトコル ハンドラー オブジェクトを一意に識別する MAPI URL が生成されます。 MAPI Url、Unicode でエンコードされた、次の形式。 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

次の表では、一般的な URL の各部分について説明します。

|パーツ | 説明|
|:----|:-----------|  
|*SID* |現在のユーザーのセキュリティ識別子です。| 
|*StoreDisplayName* |そのストア上で、ユーザーの表示名を指定する文字列です。|
|*ハッシュ番号* |計算された 16 進数表現では、 **DWORD**は、ストア エントリ ID またはストア マッピングの署名に基づいています。 この値は、レジストリに格納されているが、MAPI プロトコル ハンドラーでストアを識別するのには後で使用されます。<br/><br/>この数値は、他のストアとの衝突を最小限に抑える方法で計算する必要があります。 Microsoft Outlook を使用してハッシュを計算するアルゴリズムでは、[番号を保存するハッシュを計算するアルゴリズム](algorithm-to-calculate-the-store-hash-number.md)を参照してください。|
|*StoreType* |インデックスを作成するオブジェクトが含まれるストアの種類を識別する番号です。 使用可能な値は次のとおりです。<br/>-0 - 既定のストアです。<br/><br/>-代理ストアを 1 -、代理人のアイテムがローカルにキャッシュを使用します。<br/><br/>-2 - パブリック フォルダー、パブリック フォルダーのお気に入りを使用します。<br/><br/>**注**: ストアは、プッシュの代わりにクロールするが、使用される値が*X*の文字です。| 
|*FolderNameA/.../FolderNameN* |IPM_SUBTREE のルートからフォルダーまたはメッセージへのパスです。 たとえば、 **[受信トレイ]** の下で [**ファミリ**] フォルダーにメッセージは、このパラメーターの**受信トレイと家族**を持っています。 |
|*EntryIDEncoded* |Unicode 文字列としてエンコードされたアイテムの MAPI エントリ ID です。 特定の特殊文字をエンコードする方法については、次のセクション特殊文字」を参照してください。 エントリ ID をエンコードするためのアルゴリズムの詳細については、[アルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)を参照してください。<br/><br/>**注**: ランダムのハングル文字または使用可能なフォントに応じて、アルゴリズムに準拠しているボックスに ID が表示されるエントリがこのエンコードされたテキストとして表示するときです。  |
|*AttachIDEncoded* |Unicode 文字列としてエンコードされた添付ファイルの ID です。 特定の特殊文字をエンコードする方法については、次のセクション特殊文字」を参照してください。 エントリ ID をエンコードするためのアルゴリズムの詳細については、[アルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)を参照してください。<br/><br/>**注**: ランダムのハングル文字または使用可能なフォントに応じて、アルゴリズムに準拠しているボックスに ID が表示されるエントリがこのエンコードされたテキストとして表示するときです。 |
|*Filename* |添付ファイルの名前、メッセージに表示されるファイルです。|
    
## <a name="examples-of-mapi-urls"></a>MAPI Url の例

MAPI Url の例を次に示します。
  
- フォルダーの MAPI URL: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- メッセージの MAPI URL: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- 添付ファイルは MAPI URL: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>特殊文字

メッセージまたは添付ファイルに含まれる場合は、特定の文字がエンコードされます。 MAPI URL をエンコードする文字を次に示します。
  
- % > %25
    
- /> %2f 
    
- \ > %5 C 
    
- \*> %2a 
    
- ? > %3f 
    
## <a name="blob-associated-with-each-mapi-url"></a>各 MAPI URL に関連付けられた blob

オブジェクトのインデックスを作成する MAPI URL をプッシュするには、ストア プロバイダーは、MAPI プロトコル ハンドラーの特定の情報を格納するバイナリ ラージ オブジェクト (BLOB) をも作成します。 ストア プロバイダーは、各 MAPI URL を使用してこの BLOB に関連付けるし、MAPI URL がインデクサーにプッシュするときに送信します。 BLOB の形式は次のとおりです。 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

ストア プロバイダーは、以下の順に BLOB をこれらの値を記述する必要があります。 次の表では、BLOB の各フィールドについて説明します。

|パーツ | 説明|
|:----|:-----------|  
|*dwVersion* |これは、送信されるデータのバージョンです。 現在、この値は 1 です。|
|*dwFlags* |将来の使用のために予約されています。 現在この値は 0 を指定する必要があります。|
|*cbProfileName* |バイトで、プロファイル名のサイズです。 この情報は、MAPI プロトコル ハンドラーは、項目のインデックスを作成するときに使用するプロファイルを知っている場合に便利です。|
|*wszProfileName* |Null で終わる Unicode 文字列プロファイル名が含まれています。|
|*cbProviderItemID* |プロバイダー アイテム ID のバイト単位のサイズです。 ストア プロバイダーは、この情報を取得する追加のフォルダーを開けないようにするのには、フォルダーのアイテムの ID プロバイダーのみを送信する必要があります。|
|*wszProviderItemID* |Null で終わる Unicode 文字列ストア内の項目を一意に識別するプロバイダー アイテム ID を持つ。|
    
## <a name="see-also"></a>関連項目

- [ストアの通知に基づくインデックスの作成について](about-notification-based-store-indexing.md)
- [MAPI �萔](mapi-constants.md)

