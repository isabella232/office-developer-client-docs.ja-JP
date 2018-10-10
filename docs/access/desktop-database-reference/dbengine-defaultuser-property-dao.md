---
title: DBEngine.DefaultUser プロパティ (DAO)
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
ms.openlocfilehash: 15fc13b27b30c87bd3993b12303cc59b8a0115bf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477122"
---
# <a name="dbenginedefaultuser-property-dao"></a><span data-ttu-id="fe3a1-102">DBEngine.DefaultUser プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe3a1-102">DBEngine.DefaultUser Property (DAO)</span></span>


<span data-ttu-id="fe3a1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe3a1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fe3a1-p101">既定の **Workspace** オブジェクトを作成するために初期化時に使用されるユーザー名を設定します。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-p101">Sets the user name used to create the default **Workspace** when it is initialized. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3a1-106">構文</span><span class="sxs-lookup"><span data-stu-id="fe3a1-106">Syntax</span></span>

<span data-ttu-id="fe3a1-107">*式*です。デフォルト</span><span class="sxs-lookup"><span data-stu-id="fe3a1-107">*expression* .DefaultUser</span></span>

<span data-ttu-id="fe3a1-108">\*式\***DBEngine**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-108">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe3a1-109">注釈</span><span class="sxs-lookup"><span data-stu-id="fe3a1-109">Remarks</span></span>

<span data-ttu-id="fe3a1-110">**デフォルト**の設定は、文字列データ型です。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-110">The setting for **DefaultUser** is a String data type.</span></span> <span data-ttu-id="fe3a1-111">1 ~ 20 文字であることができます Microsoft Access では長い間ワークスペースとして含めることができますアルファベット文字、アクセント記号付き文字、数字、スペース、および記号:"(引用符は含みません)、/(スラッシュ)、 \\ (バック スラッシュ)、 \[ \] (角かっこ)、: (コロン)、|(パイプ)、 \< (以下の記号よりも)、 \> (大きい-記号よりも)、+ (プラス記号)、= (等しい記号)、です。(セミコロン)、(コンマ)、でしょうか。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-111">It can be 1–20 characters long in Microsoft Access workspaces and it can include alphabetic characters, accented characters, numbers, spaces, and symbols except for: " (quotation marks), / (forward slash), \\ (backslash), \[ \] (brackets), : (colon), | (pipe), \< (less-than sign), \> (greater-than sign), + (plus sign), = (equal sign), ; (semicolon), , ( comma), ?</span></span> <span data-ttu-id="fe3a1-112">(疑問符 ())、 \* (アスタリスク)、先頭のスペース、および制御文字 (ASCII 00 ASCII 31)。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-112">(question mark), \* (asterisk), leading spaces, and control characters (ASCII 00 to ASCII 31).</span></span>


> [!NOTE]
> <P><span data-ttu-id="fe3a1-p103">[!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></P>



<span data-ttu-id="fe3a1-118">既定では、 **DefaultUser** プロパティは "admin" に設定され、 **DefaultPassword** プロパティは長さが 0 の文字列 ("") に設定されます。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-118">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="fe3a1-p104">通常は、ユーザー名は大文字と小文字を区別しませんが、削除された、または別のワークグループで作成されたユーザー アカウントを再作成する場合、ユーザー名と元の名前は、大文字と小文字の区別まで厳密に一致している必要があります。パスワードは大文字と小文字を区別します。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-p104">User names aren't usually case-sensitive; however, if you're re-creating a user account that was deleted or created in a different workgroup, the user name must be an exact case-sensitive match of the original name. Passwords are case-sensitive.</span></span>

<span data-ttu-id="fe3a1-p105">通常は、CreateWorkspace メソッドを使用して、任意のユーザー名とパスワードを持つ Workspace オブジェクトを作成します。ただし、以前のバージョンとの互換性を保つため、およびセキュリティで保護されたデータベースを実装しない場合に便宜を図るために、Workspace オブジェクトがまだ開いていなければ、必要に応じて既定の Workspace オブジェクトが自動的に作成されます。この場合、DefaultUser プロパティと DefaultPassword プロパティの値により、既定の Workspace オブジェクトのユーザーとパスワードが定義されます。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-p105">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="fe3a1-124">このプロパティを有効にするには、DAO メソッドを呼び出す前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe3a1-124">For this property to take effect, you should set it before calling any DAO methods.</span></span>

