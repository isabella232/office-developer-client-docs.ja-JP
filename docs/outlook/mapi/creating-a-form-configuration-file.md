---
title: フォーム構成ファイルを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9ceb7ad347e73f69eca3463ed2edc4438a45a21f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799860"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="88e46-103">フォーム構成ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="88e46-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="88e46-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88e46-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88e46-105">フォーム構成ファイルは、フォーム マネージャーを使用しているとクライアント アプリケーションの両方のフォームに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="88e46-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="88e46-106">フォーム構成ファイルには、メッセージング クライアント、フォームによって実装された動詞およびフォームでサポートされているプラットフォームで使用するフォームによって公開されたプロパティを含むフォームの場合、広範な仕様が含まれています。</span><span class="sxs-lookup"><span data-stu-id="88e46-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="88e46-107">フォーム構成ファイルは、.cfg ファイルの拡張子を持つファイル、Windows の初期化ファイルのような形式には</span><span class="sxs-lookup"><span data-stu-id="88e46-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="88e46-108">プレーン テキスト ファイル セクションの数とすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="88e46-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="88e46-109">各セクションは、セクション名を角かっこで囲まれているから始まります。</span><span class="sxs-lookup"><span data-stu-id="88e46-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="88e46-110">各セクションには、値およびそのセクションに関連する設定を定義する 1 つまたは複数の行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="88e46-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="88e46-111">次の種類のいずれかの値があります。</span><span class="sxs-lookup"><span data-stu-id="88e46-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="88e46-112">String</span><span class="sxs-lookup"><span data-stu-id="88e46-112">String</span></span>
    
- <span data-ttu-id="88e46-113">表示される文字列</span><span class="sxs-lookup"><span data-stu-id="88e46-113">Displayed string</span></span>
    
- <span data-ttu-id="88e46-114">プラットフォームの文字列</span><span class="sxs-lookup"><span data-stu-id="88e46-114">Platform string</span></span>
    
- <span data-ttu-id="88e46-115">パス名</span><span class="sxs-lookup"><span data-stu-id="88e46-115">Path name</span></span>
    
- <span data-ttu-id="88e46-116">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="88e46-116">Integer</span></span>
    
- <span data-ttu-id="88e46-117">GUID</span><span class="sxs-lookup"><span data-stu-id="88e46-117">GUID</span></span>
    
<span data-ttu-id="88e46-118">.Cfg ファイルのセクションの詳細については、[フォーム構成ファイルの形式のファイル](file-format-of-form-configuration-files.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88e46-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="88e46-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="88e46-119">See also</span></span>



[<span data-ttu-id="88e46-120">MAPI フォームのサーバーの開発</span><span class="sxs-lookup"><span data-stu-id="88e46-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

