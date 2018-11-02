---
title: DBEngine.DefaultPassword プロパティ (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 705bd14208b3a6b07b7d5adddfc4f1fdf36928c5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924604"
---
# <a name="dbenginedefaultpassword-property-dao"></a><span data-ttu-id="10d21-102">DBEngine.DefaultPassword プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="10d21-102">DBEngine.DefaultPassword property (DAO)</span></span>


<span data-ttu-id="10d21-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="10d21-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10d21-p101">既定の **Workspace** を作成するために初期化時に使用されるパスワードを設定します。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="10d21-p101">Sets the password used to create the default **Workspace** when it is initialized. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d21-106">構文</span><span class="sxs-lookup"><span data-stu-id="10d21-106">Syntax</span></span>

<span data-ttu-id="10d21-107">*式*です。DefaultPassword</span><span class="sxs-lookup"><span data-stu-id="10d21-107">*expression* .DefaultPassword</span></span>

<span data-ttu-id="10d21-108">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="10d21-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="10d21-109">注釈</span><span class="sxs-lookup"><span data-stu-id="10d21-109">Remarks</span></span>

<span data-ttu-id="10d21-p102">**DefaultPassword** の設定値は、最大 20 文字の文字列データ型 (String) です。このプロパティには、ASCII の 0 を除くすべての文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="10d21-p102">The setting for **DefaultPassword** is a String data type that can be up to 20 characters long. It can contain any character except ASCII 0.</span></span>


> [!NOTE]
> <span data-ttu-id="10d21-p103">[!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="10d21-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="10d21-117">既定では、 **DefaultUser** プロパティは "admin" に設定され、 **DefaultPassword** プロパティは長さが 0 の文字列 ("") に設定されます。</span><span class="sxs-lookup"><span data-stu-id="10d21-117">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="10d21-p104">通常は、CreateWorkspace メソッドを使用して、任意のユーザー名とパスワードを持つ Workspace オブジェクトを作成します。ただし、以前のバージョンとの互換性を保つため、およびセキュリティで保護されたデータベースを実装しない場合に便宜を図るために、Workspace オブジェクトがまだ開いていなければ、必要に応じて既定の Workspace オブジェクトが自動的に作成されます。この場合、DefaultUser プロパティと DefaultPassword プロパティの値により、既定の Workspace オブジェクトのユーザーとパスワードが定義されます。</span><span class="sxs-lookup"><span data-stu-id="10d21-p104">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="10d21-121">このプロパティを有効にするには、DAO メソッドを呼び出す前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10d21-121">For this property to take effect, you should set it before calling any DAO methods.</span></span>

