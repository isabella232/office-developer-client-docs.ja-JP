---
title: ChangePassword メソッド (ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 34de673d29d160c715c8e2617d0e2a75e3843904
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872236"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="fef7a-102">ChangePassword メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="fef7a-102">ChangePassword Method (ADOX)</span></span>


<span data-ttu-id="fef7a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fef7a-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="fef7a-104">ユーザー アカウントのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="fef7a-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef7a-105">構文</span><span class="sxs-lookup"><span data-stu-id="fef7a-105">Syntax</span></span>

<span data-ttu-id="fef7a-106">*ユーザー*です。パスワードの変更を*OldPassword*、 *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="fef7a-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="fef7a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fef7a-107">Parameters</span></span>

  - <span data-ttu-id="fef7a-108">*OldPassword*</span><span class="sxs-lookup"><span data-stu-id="fef7a-108">*OldPassword*</span></span>

  - <span data-ttu-id="fef7a-p101">ユーザーの現在のパスワードを示す文字列型 (**String**) の値を指定します。ユーザーが現在パスワードを使用していない場合は、*OldPassword* に空の文字列 ("") を指定してください。</span><span class="sxs-lookup"><span data-stu-id="fef7a-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

  - <span data-ttu-id="fef7a-111">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="fef7a-111">*NewPassword*</span></span>

  - <span data-ttu-id="fef7a-112">新しいパスワードを表す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="fef7a-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="fef7a-113">解説</span><span class="sxs-lookup"><span data-stu-id="fef7a-113">Remarks</span></span>

<span data-ttu-id="fef7a-114">セキュリティ上の理由から、新規パスワードに加え、古いパスワードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fef7a-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="fef7a-115">プロバイダーがトラスティ プロパティの管理をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="fef7a-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

