---
title: DCOM を使用できるようにクライアント上にビジネス オブジェクトを登録する
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7479eefcc975ca0fe7bb7fe0d51796d1b1f416b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307097"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a><span data-ttu-id="6164f-102">DCOM を使用できるようにクライアント上にビジネス オブジェクトを登録する</span><span class="sxs-lookup"><span data-stu-id="6164f-102">Registering business objects on the client for use with DCOM</span></span>

<span data-ttu-id="6164f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6164f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6164f-p101">カスタム ビジネス オブジェクトは、DCOM を介して使用できる識別子 (CLSID) にクライアント側がプログラム名 (ProgId) を確実にマップできるようにしておく必要があります。このため、DCOM オブジェクトの ProgID をクライアント側のレジストリに指定し、サーバー側ビジネス オブジェクトのクラス ID にマップする必要があります。サポートされている他のプロトコル (HTTP、HTTPS、およびインプロセス) では、この操作は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6164f-p101">Custom business objects need to ensure that the client side can map their program name (ProgId) to an identifier (CLSID) that can be used over DCOM. For this reason, the ProgID of the DCOM object must be in the client-side registry and map to the class ID of the server-side business object. For the other supported protocols (HTTP, HTTPS, and in-process), this is not necessary.</span></span>

<span data-ttu-id="6164f-107">たとえば、MyBObj という名前のサーバー側ビジネス オブジェクトを "{00112233-4455-6677-8899-00AABBCCDDEE}" という特定のクラス ID に公開する場合、次のエントリがクライアント側のレジストリに追加されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6164f-107">For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

