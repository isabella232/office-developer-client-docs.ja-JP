---
title: Try_Parse 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: 指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307799"
---
# <a name="tryparse-function-access-custom-web-app"></a><span data-ttu-id="58f56-103">Try_Parse 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="58f56-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="58f56-104">指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。</span><span class="sxs-lookup"><span data-stu-id="58f56-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="58f56-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="58f56-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="58f56-107">構文</span><span class="sxs-lookup"><span data-stu-id="58f56-107">Syntax</span></span>

 <span data-ttu-id="58f56-108">**Try_Parse**(*textexpression*、 *DataType*)</span><span class="sxs-lookup"><span data-stu-id="58f56-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="58f56-109">**Try_Parse** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="58f56-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="58f56-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="58f56-110">**Argument name**</span></span>|<span data-ttu-id="58f56-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="58f56-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="58f56-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="58f56-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="58f56-113">指定したデータ型になっているか解析される対象の、書式設定された値を表すテキスト式。</span><span class="sxs-lookup"><span data-stu-id="58f56-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="58f56-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="58f56-114">*DataType*</span></span>  <br/> |<span data-ttu-id="58f56-115">*textexpression*を解析するデータ型。</span><span class="sxs-lookup"><span data-stu-id="58f56-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58f56-116">解説</span><span class="sxs-lookup"><span data-stu-id="58f56-116">Remarks</span></span>

<span data-ttu-id="58f56-p102">**Try_Parse** は、文字列型から日付/時刻型および数値型への変換にのみ使用します。一般的な型変換では、引き続き **Convert** を使用します。</span><span class="sxs-lookup"><span data-stu-id="58f56-p102">Use **Try_Parse** only for converting from string to date/time and number types. For general type conversions, continue to use **Convert**.</span></span> 
  

