---
title: DCOM を使用できるようにクライアント上にビジネス オブジェクトを登録する
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5a63a2af1a5cadd112cfc1f75471247c7481115b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557877"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>DCOM を使用できるようにクライアント上にビジネス オブジェクトを登録する

**適用先:** Access 2013、Office 2013

カスタム ビジネス オブジェクトは、DCOM を介して使用できる識別子 (CLSID) にクライアント側がプログラム名 (ProgId) を確実にマップできるようにしておく必要があります。このため、DCOM オブジェクトの ProgID をクライアント側のレジストリに指定し、サーバー側ビジネス オブジェクトのクラス ID にマップする必要があります。サポートされている他のプロトコル (HTTP、HTTPS、およびインプロセス) では、この操作は必要ありません。

たとえば、MyBObj という名前のサーバー側ビジネス オブジェクトを "{00112233-4455-6677-8899-00AABBCCDDEE}" という特定のクラス ID に公開する場合、次のエントリがクライアント側のレジストリに追加されていることを確認する必要があります。

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

