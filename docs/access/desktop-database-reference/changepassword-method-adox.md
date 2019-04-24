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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296529"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="ca58e-102">ChangePassword メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ca58e-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="ca58e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca58e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca58e-104">ユーザー アカウントのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="ca58e-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca58e-105">構文</span><span class="sxs-lookup"><span data-stu-id="ca58e-105">Syntax</span></span>

<span data-ttu-id="ca58e-106">*ユーザー*。ChangePassword*oldpassword*, *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="ca58e-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="ca58e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca58e-107">Parameters</span></span>

|<span data-ttu-id="ca58e-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca58e-108">Parameter</span></span>|<span data-ttu-id="ca58e-109">説明</span><span class="sxs-lookup"><span data-stu-id="ca58e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ca58e-110">*oldpassword*</span><span class="sxs-lookup"><span data-stu-id="ca58e-110">*OldPassword*</span></span> |<span data-ttu-id="ca58e-111">ユーザーの現在のパスワードを示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca58e-111">A **String** value that specifies the user's existing password.</span></span> <span data-ttu-id="ca58e-112">ユーザーが現在パスワードを使用していない場合は、*OldPassword* に空の文字列 ("") を指定してください。</span><span class="sxs-lookup"><span data-stu-id="ca58e-112">If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="ca58e-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="ca58e-113">*NewPassword*</span></span> |<span data-ttu-id="ca58e-114">新しいパスワードを表す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca58e-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ca58e-115">注釈</span><span class="sxs-lookup"><span data-stu-id="ca58e-115">Remarks</span></span>

<span data-ttu-id="ca58e-116">セキュリティ上の理由から、新規パスワードに加え、古いパスワードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca58e-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="ca58e-117">プロバイダーがトラスティ プロパティの管理をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ca58e-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

