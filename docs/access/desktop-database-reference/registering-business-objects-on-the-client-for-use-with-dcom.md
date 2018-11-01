---
title: DCOM を使用してビジネス オブジェクトをクライアントに登録する
TOCTitle: Registering Business Objects on the Client for Use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9b106fa88df8205595312aaebdabf82cf12d57c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887811"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a><span data-ttu-id="856b2-102">DCOM を使用してビジネス オブジェクトをクライアントに登録する</span><span class="sxs-lookup"><span data-stu-id="856b2-102">Registering Business Objects on the Client for Use with DCOM</span></span>


<span data-ttu-id="856b2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="856b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="856b2-p101">カスタム ビジネス オブジェクトは、DCOM を介して使用できる識別子 (CLSID) にクライアント側がプログラム名 (ProgId) を確実にマップできるようにしておく必要があります。このため、DCOM オブジェクトの ProgID をクライアント側のレジストリに指定し、サーバー側ビジネス オブジェクトのクラス ID にマップする必要があります。サポートされている他のプロトコル (HTTP、HTTPS、およびインプロセス) では、この操作は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="856b2-p101">Custom business objects need to ensure that the client side can map their program name (ProgId) to an identifier (CLSID) that can be used over DCOM. For this reason, the ProgID of the DCOM object must be in the client-side registry and map to the class ID of the server-side business object. For the other supported protocols (HTTP, HTTPS, and in-process), this is not necessary.</span></span>

<span data-ttu-id="856b2-107">たとえば、MyBObj という名前のサーバー側ビジネス オブジェクトを "{00112233-4455-6677-8899-00AABBCCDDEE}" という特定のクラス ID に公開する場合、次のエントリがクライアント側のレジストリに追加されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="856b2-107">For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

