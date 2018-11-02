---
title: Database.NewPassword メソッド (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f4dca778da3c364d9e9b5a5eaf8ebbc32501853f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919361"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="c3f5d-102">Database.NewPassword メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="c3f5d-102">Database.NewPassword method (DAO)</span></span>


<span data-ttu-id="c3f5d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3f5d-104">既存の Microsoft Access データベース エンジンのデータベースのパスワードを変更します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f5d-105">構文</span><span class="sxs-lookup"><span data-stu-id="c3f5d-105">Syntax</span></span>

<span data-ttu-id="c3f5d-106">*式*です。NewPassword (***bstrOld***、 ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="c3f5d-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="c3f5d-107">\*式\***データベース**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-107">*expression* An expression that returns a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c3f5d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c3f5d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3f5d-109">名前</span><span class="sxs-lookup"><span data-stu-id="c3f5d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c3f5d-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="c3f5d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c3f5d-111">データ型</span><span class="sxs-lookup"><span data-stu-id="c3f5d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c3f5d-112">説明</span><span class="sxs-lookup"><span data-stu-id="c3f5d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3f5d-113">bstrOld</span><span class="sxs-lookup"><span data-stu-id="c3f5d-113">bstrOld</span></span></p></td>
<td><p><span data-ttu-id="c3f5d-114">必須</span><span class="sxs-lookup"><span data-stu-id="c3f5d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="c3f5d-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="c3f5d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c3f5d-116"><strong>Database</strong> オブジェクトの <strong>Password</strong> プロパティの現在の設定値。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3f5d-117">bstrNew</span><span class="sxs-lookup"><span data-stu-id="c3f5d-117">bstrNew</span></span></p></td>
<td><p><span data-ttu-id="c3f5d-118">必須</span><span class="sxs-lookup"><span data-stu-id="c3f5d-118">Required</span></span></p></td>
<td><p><span data-ttu-id="c3f5d-119"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="c3f5d-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c3f5d-120"><strong>Database</strong>オブジェクトの<strong>Password</strong>プロパティの新しい設定します。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>

> [!NOTE]
> <span data-ttu-id="c3f5d-p101">大文字、小文字、数字、記号を組み合わせた強力なパスワードを使用してください。これらの文字を混在させていないパスワードは脆弱なパスワードです。Y6dh!et5 は強力なパスワードです。House27 は脆弱なパスワードです。強力なパスワードでありながら、書き留めておかなくても覚えておくことができるパスワードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-p101">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c3f5d-126">注釈</span><span class="sxs-lookup"><span data-stu-id="c3f5d-126">Remarks</span></span>

<span data-ttu-id="c3f5d-127">BstrOld および bstrNew の文字列は、長さは最大 20 文字し、ASCII 文字 0 (null) 以外の任意の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="c3f5d-128">パスワードをクリアするには、長さ 0 の文字列を使用します ("") bstrNew のです。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="c3f5d-129">パスワードでは、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="c3f5d-130">データベースにパスワードが設定されていない場合は、古いパスワードとして長さ 0 の文字列 ("") が渡され、自動的にパスワードが生成されます。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="c3f5d-131">[!重要] パスワードを紛失した場合、そのデータベースを二度と開けなくなります。</span><span class="sxs-lookup"><span data-stu-id="c3f5d-131">If you lose your password, you can never open the database again.</span></span>


