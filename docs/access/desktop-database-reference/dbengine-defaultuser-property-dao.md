---
title: DBEngine ユーザープロパティ (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c29f9663ce3591fe5b1633239e8ec0d8866ee16a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294348"
---
# <a name="dbenginedefaultuser-property-dao"></a><span data-ttu-id="a27d3-102">DBEngine ユーザープロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a27d3-102">DBEngine.DefaultUser property (DAO)</span></span>


<span data-ttu-id="a27d3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a27d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a27d3-104">初期化されたときに、既定の**Workspace**オブジェクトを作成するために使用されるユーザー名を設定します。</span><span class="sxs-lookup"><span data-stu-id="a27d3-104">Sets the user name used to create the default **Workspace** when it is initialized.</span></span> <span data-ttu-id="a27d3-105">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="a27d3-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a27d3-106">構文</span><span class="sxs-lookup"><span data-stu-id="a27d3-106">Syntax</span></span>

<span data-ttu-id="a27d3-107">*式*。DefaultUser</span><span class="sxs-lookup"><span data-stu-id="a27d3-107">*expression* .DefaultUser</span></span>

<span data-ttu-id="a27d3-108">\*式\***DBEngine**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a27d3-108">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a27d3-109">注釈</span><span class="sxs-lookup"><span data-stu-id="a27d3-109">Remarks</span></span>

<span data-ttu-id="a27d3-110">The setting for **DefaultUser** is a String data type.</span><span class="sxs-lookup"><span data-stu-id="a27d3-110">The setting for **DefaultUser** is a String data type.</span></span> <span data-ttu-id="a27d3-111">Microsoft access ワークスペースでは 1 ~ 20 文字の長さにすることができます。また、: "(引用符),/(スラッシュ), \\ (円記号) \[ \] , (かっこ) のように、英数字、アクセント記号付きの文字、数字、スペース、記号を含めることができます。、: (コロン)、|(パイプ)、 \< (不等号)、 \> (不等号)、+ (正符号)、= (等号)、、、。(セミコロン)、、(コンマ)、?</span><span class="sxs-lookup"><span data-stu-id="a27d3-111">It can be 1–20 characters long in Microsoft Access workspaces and it can include alphabetic characters, accented characters, numbers, spaces, and symbols except for: " (quotation marks), / (forward slash), \\ (backslash), \[ \] (brackets), : (colon), | (pipe), \< (less-than sign), \> (greater-than sign), + (plus sign), = (equal sign), ; (semicolon), , ( comma), ?</span></span> <span data-ttu-id="a27d3-112">(疑問符)、 \* (アスタリスク)、先頭のスペース、制御文字 (ascii 00 ~ ascii 31)。</span><span class="sxs-lookup"><span data-stu-id="a27d3-112">(question mark), \* (asterisk), leading spaces, and control characters (ASCII 00 to ASCII 31).</span></span>


> [!NOTE]
> <span data-ttu-id="a27d3-p103">[!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="a27d3-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="a27d3-118">既定では、 **DefaultUser** プロパティは "admin" に設定され、 **DefaultPassword** プロパティは長さが 0 の文字列 ("") に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a27d3-118">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="a27d3-p104">通常は、ユーザー名は大文字と小文字を区別しませんが、削除された、または別のワークグループで作成されたユーザー アカウントを再作成する場合、ユーザー名と元の名前は、大文字と小文字の区別まで厳密に一致している必要があります。パスワードは大文字と小文字を区別します。</span><span class="sxs-lookup"><span data-stu-id="a27d3-p104">User names aren't usually case-sensitive; however, if you're re-creating a user account that was deleted or created in a different workgroup, the user name must be an exact case-sensitive match of the original name. Passwords are case-sensitive.</span></span>

<span data-ttu-id="a27d3-p105">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span><span class="sxs-lookup"><span data-stu-id="a27d3-p105">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="a27d3-124">このプロパティを有効にするには、DAO メソッドを呼び出す前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a27d3-124">For this property to take effect, you should set it before calling any DAO methods.</span></span>

