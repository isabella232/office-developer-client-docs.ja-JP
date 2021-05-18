---
title: アドレス帳を開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6d1a7e8e1d9debd7eb715bbe4958657c000f1e6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404548"
---
# <a name="opening-the-address-book"></a><span data-ttu-id="e4bef-103">アドレス帳を開く</span><span class="sxs-lookup"><span data-stu-id="e4bef-103">Opening the address book</span></span>

<span data-ttu-id="e4bef-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4bef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4bef-p101">���M��[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)�𓝍����ꂽ�A�h���X����J���AMAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)�C���^�[�t�F�C�X�ւ̃|�C���^�[��擾���܂��B���ׂẴv���t�@�C���ŃA�h���X���̃v���o�C�_�[�̊e�R���e�i�[��̍��ڂɃA�N�Z�X���� **IAddrBook**�C���^�[�t�F�C�X�̃��\�b�h��g�p���邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="e4bef-p101">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span></span> 
  
<span data-ttu-id="e4bef-p102">**OpenAddressBook**�x���AMAPI_W_ERRORS_RETURNED�A�A�h���X���̃v���o�C�_�[�� 1 �ȏ�̖�肪�����������Ƃ������Ԃ����Ƃ�����܂��B�Θb�^�̃N���C�A���g�K�v������܂�[IMAPISession::GetLastError](imapisession-getlasterror.md)��Ăяo�� **OpenAddressBook**�Ԃ��ꂽ���A�ŏ��̎��Ԃ�\�����邻�̑��̃G���[����擾���A�x�����Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e4bef-p102">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span></span> 
  
<span data-ttu-id="e4bef-p103">�Θb�^�̃N���C�A���g���x���𖳎����Ă̕��@�����������ꍇ�A�菇�ɐi�݂܂��B�Ԃ���� **IAddrBook**�C���^�[�t�F�C�X���L�����ǂ����Ɋ֌W�Ȃ����ׂāA�ꕔ�A�܂��̓A�h���X���v���o�C�_�[ �v���t�@�C����� [�Ȃ�] ����s���Ă��܂��B���̂��߁A�Z�b�V�������I�������Ƃ��ɁA **IAddrBook**�|�C���^�[��������Θb�^�ƑΘb�^�̗����̃N���C�A���g��o���Ă����Ă��������B</span><span class="sxs-lookup"><span data-stu-id="e4bef-p103">Noninteractive clients should ignore the warning and proceed as if the method succeeded. The returned **IAddrBook** interface is valid regardless of whether all, some, or none of the address book providers in the profile are running. Therefore, both interactive and noninteractive clients must always remember to release the **IAddrBook** pointer when the session ends.</span></span> 
  

