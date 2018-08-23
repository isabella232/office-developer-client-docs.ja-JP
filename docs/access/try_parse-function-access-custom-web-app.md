---
title: Try_Parse 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: 指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798756"
---
# <a name="tryparse-function-access-custom-web-app"></a><span data-ttu-id="29e1a-103">Try_Parse 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="29e1a-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="29e1a-104">指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。</span><span class="sxs-lookup"><span data-stu-id="29e1a-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="29e1a-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="29e1a-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="29e1a-107">構文</span><span class="sxs-lookup"><span data-stu-id="29e1a-107">Syntax</span></span>

 <span data-ttu-id="29e1a-108">**Try_Parse**(*TextExpression*、*データ型*)</span><span class="sxs-lookup"><span data-stu-id="29e1a-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="29e1a-109">**Try_Parse** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="29e1a-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="29e1a-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="29e1a-110">**Argument name**</span></span>|<span data-ttu-id="29e1a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="29e1a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="29e1a-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="29e1a-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="29e1a-113">指定したデータ型に解析する、書式設定された値を表す文字列式を指定します。</span><span class="sxs-lookup"><span data-stu-id="29e1a-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="29e1a-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="29e1a-114">*DataType*</span></span>  <br/> |<span data-ttu-id="29e1a-115">*TextExpression*を解析するためにデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="29e1a-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29e1a-116">解説</span><span class="sxs-lookup"><span data-stu-id="29e1a-116">Remarks</span></span>

<span data-ttu-id="29e1a-p102">**Try_Parse** は、文字列型から日付/時刻型および数値型への変換にのみ使用します。一般的な型変換では、引き続き **Convert** を使用します。</span><span class="sxs-lookup"><span data-stu-id="29e1a-p102">Use **Try_Parse** only for converting from string to date/time and number types. For general type conversions, continue to use **Convert**.</span></span> 
  

