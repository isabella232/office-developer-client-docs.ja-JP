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
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708670"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="94c76-102">Database.NewPassword メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="94c76-102">Database.NewPassword method (DAO)</span></span>

<span data-ttu-id="94c76-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="94c76-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94c76-104">既存の Microsoft Access データベース エンジンのデータベースのパスワードを変更します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="94c76-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="94c76-105">構文</span><span class="sxs-lookup"><span data-stu-id="94c76-105">Syntax</span></span>

<span data-ttu-id="94c76-106">*式*です。NewPassword (***bstrOld***、 ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="94c76-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="94c76-107">\*式\***データベース**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="94c76-107">*expression* An expression that returns a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="94c76-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="94c76-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94c76-109">名前</span><span class="sxs-lookup"><span data-stu-id="94c76-109">Name</span></span></p></th>
<th><p><span data-ttu-id="94c76-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="94c76-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="94c76-111">データ型</span><span class="sxs-lookup"><span data-stu-id="94c76-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="94c76-112">説明</span><span class="sxs-lookup"><span data-stu-id="94c76-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94c76-113"><em>bstrOld</em></span><span class="sxs-lookup"><span data-stu-id="94c76-113"><em>bstrOld</em></span></span></p></td>
<td><p><span data-ttu-id="94c76-114">必須</span><span class="sxs-lookup"><span data-stu-id="94c76-114">Required</span></span></p></td>
<td><p><span data-ttu-id="94c76-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="94c76-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="94c76-116"><strong>Database</strong> オブジェクトの <strong>Password</strong> プロパティの現在の設定値。</span><span class="sxs-lookup"><span data-stu-id="94c76-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94c76-117"><em>bstrNew</em></span><span class="sxs-lookup"><span data-stu-id="94c76-117"><em>bstrNew</em></span></span></p></td>
<td><p><span data-ttu-id="94c76-118">必須</span><span class="sxs-lookup"><span data-stu-id="94c76-118">Required</span></span></p></td>
<td><p><span data-ttu-id="94c76-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="94c76-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="94c76-120"><strong>Database</strong>オブジェクトの<strong>Password</strong>プロパティの新しい設定します。</span><span class="sxs-lookup"><span data-stu-id="94c76-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="94c76-121"><strong>注</strong>: 大文字と小文字の英字、数字、および記号を組み合わせた強力なパスワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="94c76-121"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="94c76-122">これらの文字を混在させたものになっていないパスワードは強固とはいえません。</span><span class="sxs-lookup"><span data-stu-id="94c76-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="94c76-123">たとえば、Y6dh!et5 は安全性の高いパスワードです。</span><span class="sxs-lookup"><span data-stu-id="94c76-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="94c76-124">House27 は推測されやすいパスワードです。</span><span class="sxs-lookup"><span data-stu-id="94c76-124">Weak password: House27.</span></span> <span data-ttu-id="94c76-125">また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="94c76-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="94c76-126">解説</span><span class="sxs-lookup"><span data-stu-id="94c76-126">Remarks</span></span>

<span data-ttu-id="94c76-127">BstrOld および bstrNew の文字列は、長さは最大 20 文字し、ASCII 文字 0 (null) 以外の任意の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="94c76-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="94c76-128">パスワードをクリアするには、長さ 0 の文字列を使用します ("") bstrNew のです。</span><span class="sxs-lookup"><span data-stu-id="94c76-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="94c76-129">パスワードでは、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="94c76-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="94c76-130">データベースにパスワードが設定されていない場合は、古いパスワードとして長さ 0 の文字列 ("") が渡され、自動的にパスワードが生成されます。</span><span class="sxs-lookup"><span data-stu-id="94c76-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="94c76-131">[!重要] パスワードを紛失した場合、そのデータベースを二度と開けなくなります。</span><span class="sxs-lookup"><span data-stu-id="94c76-131">If you lose your password, you can never open the database again.</span></span>


