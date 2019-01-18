---
title: ChangePassword メソッド (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713094"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="94f82-102">ChangePassword メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="94f82-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="94f82-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="94f82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94f82-104">ユーザー アカウントのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="94f82-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f82-105">構文</span><span class="sxs-lookup"><span data-stu-id="94f82-105">Syntax</span></span>

<span data-ttu-id="94f82-106">*ユーザー*です。パスワードの変更を*OldPassword*、 *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="94f82-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="94f82-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="94f82-107">Parameters</span></span>

|<span data-ttu-id="94f82-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="94f82-108">Parameter</span></span>|<span data-ttu-id="94f82-109">説明</span><span class="sxs-lookup"><span data-stu-id="94f82-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="94f82-110">*OldPassword*</span><span class="sxs-lookup"><span data-stu-id="94f82-110">*OldPassword*</span></span> |<span data-ttu-id="94f82-p101">ユーザーの現在のパスワードを示す文字列型 (**String**) の値を指定します。ユーザーが現在パスワードを使用していない場合は、*OldPassword* に空の文字列 ("") を指定してください。</span><span class="sxs-lookup"><span data-stu-id="94f82-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="94f82-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="94f82-113">*NewPassword*</span></span> |<span data-ttu-id="94f82-114">新しいパスワードを表す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="94f82-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="94f82-115">解説</span><span class="sxs-lookup"><span data-stu-id="94f82-115">Remarks</span></span>

<span data-ttu-id="94f82-116">セキュリティ上の理由から、新規パスワードに加え、古いパスワードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94f82-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="94f82-117">プロバイダーがトラスティ プロパティの管理をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="94f82-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

