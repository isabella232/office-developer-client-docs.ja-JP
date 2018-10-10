---
title: DCOM を使用してビジネス オブジェクトをクライアントに登録する
TOCTitle: Registering Business Objects on the Client for Use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f3d29d20200b6e435ffafaaa35c7f507b88b939
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477833"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>DCOM を使用してビジネス オブジェクトをクライアントに登録する


**適用されます**Access 2013 |。Office 2013

カスタム ビジネス オブジェクトは、DCOM を介して使用できる識別子 (CLSID) にクライアント側がプログラム名 (ProgId) を確実にマップできるようにしておく必要があります。このため、DCOM オブジェクトの ProgID をクライアント側のレジストリに指定し、サーバー側ビジネス オブジェクトのクラス ID にマップする必要があります。サポートされている他のプロトコル (HTTP、HTTPS、およびインプロセス) では、この操作は必要ありません。

たとえば、MyBObj という名前のサーバー側ビジネス オブジェクトを "{00112233-4455-6677-8899-00AABBCCDDEE}" という特定のクラス ID に公開する場合、次のエントリがクライアント側のレジストリに追加されていることを確認する必要があります。

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

