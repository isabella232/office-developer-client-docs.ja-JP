---
title: 解析関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798716"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="68c33-103">解析関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="68c33-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="68c33-104">アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。</span><span class="sxs-lookup"><span data-stu-id="68c33-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="68c33-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="68c33-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="68c33-107">構文</span><span class="sxs-lookup"><span data-stu-id="68c33-107">Syntax</span></span>

 <span data-ttu-id="68c33-108">**解析**(*TextExpression*、*データ型*)</span><span class="sxs-lookup"><span data-stu-id="68c33-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="68c33-109">**Parse** 関数には、以下の引数があります。</span><span class="sxs-lookup"><span data-stu-id="68c33-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="68c33-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="68c33-110">**Argument name**</span></span>|<span data-ttu-id="68c33-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="68c33-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="68c33-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="68c33-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="68c33-113">指定したデータ型に解析する、書式設定された値を表す文字列式を指定します。</span><span class="sxs-lookup"><span data-stu-id="68c33-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="68c33-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="68c33-114">*DataType*</span></span>  <br/> |<span data-ttu-id="68c33-115">結果として要求されるデータ型を表すリテラル値。</span><span class="sxs-lookup"><span data-stu-id="68c33-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68c33-116">注釈</span><span class="sxs-lookup"><span data-stu-id="68c33-116">Remarks</span></span>

<span data-ttu-id="68c33-p102">**Parse** は、文字列から日付/時刻または数値に型を変換する場合にのみ使用します。一般的な型変換では、 **Convert** 関数を使用します。文字列値の解析には、一定のパフォーマンス オーバーヘッドが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="68c33-p102">Use **Parse** only for converting from string to date/time and number types. For general type conversions, use the **Convert** function. Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

