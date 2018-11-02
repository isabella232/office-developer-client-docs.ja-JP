---
title: ChangePassword メソッド (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f11cfaddc99a0e10a86e0df9a7a187c4e89fc794
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921062"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="cd3be-102">ChangePassword メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cd3be-102">ChangePassword method (ADOX)</span></span>


<span data-ttu-id="cd3be-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cd3be-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="cd3be-104">ユーザー アカウントのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="cd3be-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd3be-105">構文</span><span class="sxs-lookup"><span data-stu-id="cd3be-105">Syntax</span></span>

<span data-ttu-id="cd3be-106">*ユーザー*です。パスワードの変更を*OldPassword*、 *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="cd3be-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="cd3be-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cd3be-107">Parameters</span></span>

  - <span data-ttu-id="cd3be-108">*OldPassword*</span><span class="sxs-lookup"><span data-stu-id="cd3be-108">*OldPassword*</span></span>

  - <span data-ttu-id="cd3be-p101">ユーザーの現在のパスワードを示す文字列型 (**String**) の値を指定します。ユーザーが現在パスワードを使用していない場合は、*OldPassword* に空の文字列 ("") を指定してください。</span><span class="sxs-lookup"><span data-stu-id="cd3be-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

  - <span data-ttu-id="cd3be-111">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="cd3be-111">*NewPassword*</span></span>

  - <span data-ttu-id="cd3be-112">新しいパスワードを表す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="cd3be-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd3be-113">解説</span><span class="sxs-lookup"><span data-stu-id="cd3be-113">Remarks</span></span>

<span data-ttu-id="cd3be-114">セキュリティ上の理由から、新規パスワードに加え、古いパスワードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd3be-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="cd3be-115">プロバイダーがトラスティ プロパティの管理をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="cd3be-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

