---
title: セッション
TOCTitle: Sessions
ms:assetid: d81121bb-5bf8-49fb-83c4-8d3a2ffeb978
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462099(v=office.15)
ms:contentKeyID: 55119890
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: eb47a9edb0dbbef7c1aaabcc38672f2028558c6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405890"
---
# <a name="sessions"></a><span data-ttu-id="6ef82-102">セッション</span><span class="sxs-lookup"><span data-stu-id="6ef82-102">Sessions</span></span>

<span data-ttu-id="6ef82-p101">このセクションでは、Microsoft Outlook セッションに関連するサンプル タスクを示します。セッションとは、ユーザーが Outlook にログオンしている期間のことです。Outlook のセッションは [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) クラスで表現されます。このクラスは、ログインとログアウト、ID による記憶域オブジェクトへの直接アクセス、特別な既定のフォルダーへの直接アクセス、および他のユーザーが所有するデータ ソースへのアクセスをサポートしています。唯一サポートされているデータ ソースは MAPI で、これにより、ユーザーのメール ストアに格納されているすべての Outlook データにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6ef82-p101">This section includes a sample task that pertains to Microsoft Outlook sessions. A session is a period of time during which a user logs on to Outlook. A session is represented in Outlook by the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) class. This class supports logging in and out, accessing storage objects directly by ID, accessing certain special default folders directly, and accessing data sources owned by other users. The only supported data source is MAPI, which allows access to all Outlook data stored in the user's mail stores.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6ef82-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="6ef82-108">In this section</span></span>

|<span data-ttu-id="6ef82-109">トピック</span><span class="sxs-lookup"><span data-stu-id="6ef82-109">Topic</span></span>|<span data-ttu-id="6ef82-110">説明</span><span class="sxs-lookup"><span data-stu-id="6ef82-110">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="6ef82-111">Outlook のインスタンスを取得し、サインインする</span><span class="sxs-lookup"><span data-stu-id="6ef82-111">Get and sign in to an instance of Outlook</span></span>](how-to-get-and-log-on-to-an-instance-of-outlook.md)  |<span data-ttu-id="6ef82-112">Outlook のアクティブなインスタンスを表す [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクト (ローカル コンピューターで Outlook が実行されている場合) を取得するか、Outlook の新しいインスタンスを作成して既定のプロファイルにサインインし、Outlook のそのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="6ef82-112">Obtains an [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that represents an active instance of Outlook, if there is one running on the local computer, or creates a new instance of Outlook, logs on to the default profile, and returns that instance of Outlook.</span></span>|

## <a name="see-also"></a><span data-ttu-id="6ef82-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ef82-113">See also</span></span>

- [<span data-ttu-id="6ef82-114">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="6ef82-114">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

