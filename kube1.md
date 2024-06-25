PS C:\Users\butke> docker [s
docker: '[s' is not a docker command.
See 'docker --help'
PS C:\Users\butke> docker ps
CONTAINER ID   IMAGE                  COMMAND                  CREATED       STATUS         PORTS                       NAMES
b6e285e0e53d   kindest/node:v1.30.0   "/usr/local/bin/entr…"   10 days ago   Up 6 minutes   127.0.0.1:52610->6443/tcp   local-control-plane
172c51baf476   kindest/node:v1.30.0   "/usr/local/bin/entr…"   10 days ago   Up 6 minutes                               local-worker2
84e309c428cb   kindest/node:v1.30.0   "/usr/local/bin/entr…"   10 days ago   Up 6 minutes                               local-worker
PS C:\Users\butke> cat ~/.kube/config
apiVersion: v1
clusters:
- cluster:
    certificate-authority-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSURCVENDQWUyZ0F3SUJBZ0lJTzkzWkF3cUIvR2N3RFFZSktvWklodmNOQVFFTEJRQXdGVEVUTUJFR0ExVUUKQXhNS2EzVmlaWEp1WlhSbGN6QWVGdzB5TkRBMk1UVXhNVEk0TlRSYUZ3MHpOREEyTVRNeE1UTXpOVFJhTUJVeApFekFSQmdOVkJBTVRDbXQxWW1WeWJtVjBaWE13Z2dFaU1BMEdDU3FHU0liM0RRRUJBUVVBQTRJQkR3QXdnZ0VLCkFvSUJBUURENDdacGFCUUNOcnNYRVdZSmR6ZndJTHJDRkVCb0NFc3NlYi9zbkZBMUFVdnYvLzBRWnBnV3p3cUIKZ0dZVmRQV0tNM3RPNGhWb0pYUTVtUFdsYlpvRmRyUzlDQnloRStaa2QvenRnY3pSK0dBOHRmWXNsV2Ntc09ndwpGV0NrVHl3dGpjMDE4M2dpZ1hiRjZRRVo2amxsYm1Ld0cvU1BUZExnbEVGK001OHU5cVNLRkJuaWtHeHFGT3VDCmJsVmNRTU9zdXBmdjZZWVdsTHBlYXpHdTY0eFh5TzM0Z1pYZERGazhtRlZ4cjNHR3BkYWNsQUdscng3dDgrNWoKeVZPTnVRdEN5SWZtdE41REVTbk83V3lmSXZHMHRLSDFGbTEwekFzNEhrQjNCNER5M3NaSDJvZHlkODlkWSs1egpINlN1dzhveDQyaWhub3ZoUzc4cVp2K3gzK1RoQWdNQkFBR2pXVEJYTUE0R0ExVWREd0VCL3dRRUF3SUNwREFQCkJnTlZIUk1CQWY4RUJUQURBUUgvTUIwR0ExVWREZ1FXQkJRcTdLbjZJcmhGNjJjWlZVT1V4WFVudmxHN2R6QVYKQmdOVkhSRUVEakFNZ2dwcmRXSmxjbTVsZEdWek1BMEdDU3FHU0liM0RRRUJDd1VBQTRJQkFRQ0JHRXRkVENHRgp3bmhsYXVMRllPNmt6UExubDVPRG1kV1ZhaGg0SjRSUVJmSGsrd1Q2QlV5TjU5TlRWaHVrMnE1dW5UVlVteklmCnk4VWN4YWtvNXdTRlN2QWtlUm5VUVZTVzkrY3NseWM0VDZ6TytmM1V3UEdEd0lwb0J3WU1HQThEN1dnVldyQ3QKYm5WVUhBTm53bkc2K1IzbEMxV2hDblRNNm1iZDJta2lobDVibXpiTW5KL0oyaVhHbzdndkx4cDJSalJ3T2lnZQppeVdDUVdNcDRwdUZyY0R4ZlExRGpyVmFEZ0F5Tmdvc0ZicERIdzUyUGhCZk03eU8zRmR3R0hQanpOSW5yY2M3Cml1ak5kTjR0eXA4aElaL0RhRGEyVTlxSE0veS9uN1FwSHlYSUdqQjRmQXlJdVcwT1d0VWp3Uk44eXVWdlhpR3oKbUtXRWdQYTF6WHpxCi0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K
    server: https://127.0.0.1:52050
  name: kind-locallinux
- cluster:
    certificate-authority-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSURCVENDQWUyZ0F3SUJBZ0lJT0l6Mlc3dnBGSnN3RFFZSktvWklodmNOQVFFTEJRQXdGVEVUTUJFR0ExVUUKQXhNS2EzVmlaWEp1WlhSbGN6QWVGdzB5TkRBMk1UVXhNakU1TWpWYUZ3MHpOREEyTVRNeE1qSTBNalZhTUJVeApFekFSQmdOVkJBTVRDbXQxWW1WeWJtVjBaWE13Z2dFaU1BMEdDU3FHU0liM0RRRUJBUVVBQTRJQkR3QXdnZ0VLCkFvSUJBUUR0WUF0V0JrN0hicFpha3FxcHhiN21rb3g5ZWJRcjBqNlJYMzVYRUJ3Q0xhNmJIZDVFbUNTakVkTU0KdnRjK1NBTzVQdDNLbVNXK2F2RUJLTkMvblVrL2x3UHIybHNUdmgvRnpsWU91aDMwYWFUZ25taytTQ3Z6Mk9ZSQpxTVhYdm9vbk9tS1dUekR4T0R6TmswQXJaL3pWQnZnc3NiVmZ5b0lodDlsUUpMcDNQMm8rWitKaHgrUU1MQVE1CnFHRDZEMTBvR3RiT2U2S1FNSVF6aFFiYmw3QmFCWjRNcjhwZGVnNnpSVXUyTVlDNVMyLy9NNmpPcXdUc3loMjkKQ2pKZkNvV1pwZGtWaGQ2UVZqMDc2RGlYN21oakI1RGdQNG5MdklxazVuajRDbXpTQlllcDF2ZUVZd0NKbE9qaApMRTE1NXlQRUt6QXo0QmZ0bkM4eTRwOUtocnRSQWdNQkFBR2pXVEJYTUE0R0ExVWREd0VCL3dRRUF3SUNwREFQCkJnTlZIUk1CQWY4RUJUQURBUUgvTUIwR0ExVWREZ1FXQkJSZjRXRWJhQkZsT3lBWGhKakZFNU5ERTloL1JEQVYKQmdOVkhSRUVEakFNZ2dwcmRXSmxjbTVsZEdWek1BMEdDU3FHU0liM0RRRUJDd1VBQTRJQkFRQTl5TVhvQ0ZoQwpQSGFTK0NHSGxtNXNwNEZDM3A3eS85TGJsL2tpNkpDWFRRRldsZ2o4NDUxd1BJeWhmVCtlUVN1N2gwQTlZM3pWCk1FbEdIekFqYmpEM3dYY0NTd1cxKzJjd3Z4Ry9kMTdwRzFLWXRXb1ZOdFJqOGNMNDBaZ3Z5SytlZW54N0ZqQ1oKcTUybm9QVTFmeGRwWWxmeFV5cEFjK2dqeEwrZG5lN3VtaFZGRXRCT1U2dDJLUW84NzVOeG1qdXBibDhqZi9idApLclNaaVRDNWEvd2g3SXhPMXRCblJJNlZUVkRZUm1LTHlUKzdJWFVyTEp6VjZZU21NY1cwR2tUaDJYR1kxSVJwClJrdTR2NVpmL3RFV0tDM2lSVXlGM2RibHZaQ2lmRjV3UVYrWXB2ZnphM0RHMlNGWDlCVWRwL1FsdzFGSGNWUGUKcGZPMStaYndYZGdHCi0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K
    server: https://127.0.0.1:52610
  name: kind-local
contexts:
- context:
    cluster: kind-locallinux
    user: kind-locallinux
  name: kind-locallinux
- context:
    cluster: kind-local
    user: kind-local
  name: kind-local
current-context: kind-local
kind: Config
preferences: {}
users:
- name: kind-locallinux
  user:
    client-certificate-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSURLVENDQWhHZ0F3SUJBZ0lJVXUzRjFERnVPajR3RFFZSktvWklodmNOQVFFTEJRQXdGVEVUTUJFR0ExVUUKQXhNS2EzVmlaWEp1WlhSbGN6QWVGdzB5TkRBMk1UVXhNVEk0TlRSYUZ3MHlOVEEyTVRVeE1UTXpOVFZhTUR3eApIekFkQmdOVkJBb1RGbXQxWW1WaFpHMDZZMngxYzNSbGNpMWhaRzFwYm5NeEdUQVhCZ05WQkFNVEVHdDFZbVZ5CmJtVjBaWE10WVdSdGFXNHdnZ0VpTUEwR0NTcUdTSWIzRFFFQkFRVUFBNElCRHdBd2dnRUtBb0lCQVFEWUJZTHkKRWZQNUVERXF2WEZ5NjFuRGxVanVZZElRMGNlaXkwYWwxck9RaExVL21UWDBGTFFjOWRrVWo4VjZOS3RsTGpDYQpSR3ZkSkxxdnJsOGxRVUV3WnNRNlJoRE44OFlleFRKVjcxck5zM2RBbDJNWkhWbGJtZVd2MWpmRncxUjVxKzRKCkgyOHcremtUcFlOREZtUnd5K2RCMGdmZEY0UlZRejJrZHBqZ05ZSm9uSTZicExkaU83T1oyY3E2T0RXOFRJUUMKVW1zdTJ2dWk0K1k0RUZBT0JkYmgwdWZxT2RMR2tIOCtia2tGVFRxQm10TUtDYjRsR3BmaDdyUHlpSktRVzZWOQppTEdhQjhNZWJwNU9GR2ZnaGVMNGpWUWpIcXN3UWpPMGllNzNLTWl4WkZIMGp1QkRDZkd5OEhJMG9GcE14SXM1CjF4S05xbk11N2xkSElCcFhBZ01CQUFHalZqQlVNQTRHQTFVZER3RUIvd1FFQXdJRm9EQVRCZ05WSFNVRUREQUsKQmdnckJnRUZCUWNEQWpBTUJnTlZIUk1CQWY4RUFqQUFNQjhHQTFVZEl3UVlNQmFBRkNyc3Fmb2l1RVhyWnhsVgpRNVRGZFNlK1VidDNNQTBHQ1NxR1NJYjNEUUVCQ3dVQUE0SUJBUUFXcEVhWWJzWHJ0V0E1d1AreTh4TnpvYkZnCmd0NkY4QmwxUlk4eXYxVzIwUlNyWklYVmZNUXRDTE1CLzhGcVd2Mm5oQ0JhNFFoT2RzbE1hSmhaUlJkR0Y4TnkKWExPSWFGVkNWU0Jhbk43bVVWWXdEV05LYlJOUURHRVlUSDZRd0RnNi9HSVFiTFltNGEvcEpBSS9ONWk3UzJjMApZb2JONW9PK3RiUWpzUU9HckgxY05FRXU1bVdJZWdML1BhQ2JXY0JsTFNXRTFvclgwMGY0TTNLRmdoK0JHblh0CndBcjY4dHEzTUlzUXcvSWxQQmVyYWEyL2x1bkJSaTFWK2FaTFkrbXRuTFB4ZDBwaWVjUzlrcFUrWXRveGY0RXcKNFM4RGpOb2d5NTNjNDVCdUhFcWh2UlBRV0ZEN1piaTZHa3ZwYTB5eU1IWmkxSW9Dc0twQ1g1SWszVll5Ci0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K
    client-key-data: LS0tLS1CRUdJTiBSU0EgUFJJVkFURSBLRVktLS0tLQpNSUlFcEFJQkFBS0NBUUVBMkFXQzhoSHorUkF4S3IxeGN1dFp3NVZJN21IU0VOSEhvc3RHcGRhemtJUzFQNWsxCjlCUzBIUFhaRkkvRmVqU3JaUzR3bWtScjNTUzZyNjVmSlVGQk1HYkVPa1lRemZQR0hzVXlWZTlhemJOM1FKZGoKR1IxWlc1bmxyOVkzeGNOVWVhdnVDUjl2TVBzNUU2V0RReFprY012blFkSUgzUmVFVlVNOXBIYVk0RFdDYUp5TwptNlMzWWp1em1kbkt1amcxdkV5RUFsSnJMdHI3b3VQbU9CQlFEZ1hXNGRMbjZqblN4cEIvUG01SkJVMDZnWnJUCkNnbStKUnFYNGU2ejhvaVNrRnVsZllpeG1nZkRIbTZlVGhSbjRJWGkrSTFVSXg2ck1FSXp0SW51OXlqSXNXUlIKOUk3Z1F3bnhzdkJ5TktCYVRNU0xPZGNTamFwekx1NVhSeUFhVndJREFRQUJBb0lCQVFDMmVzbG50VFN6NHpLMQpXUHg1eUVlMmlPZm52eWhWWHZCV0c0TWRXaVdyWWY4OXJ5MjlkclBEZHdZZWNXaXUxOGtsR29TaC9FUmx0YjRoCjQ1bXAvZHFVaVdzZmtzcGxQNVRQcjJMYTV1dDhzaXA5bktSd3RiTWpSdmlZdGN1OU9raWswMUNyMGlyNlpHMk4KcEJZaTJNcVY0aGtESituT29Tdi9YbUszQ0J3UjRIUnZ3ZEU3cXIzdUxZSS90aVB3emJXY2FNSmVvWldPcHdBcQpSWW01S1BiNjFReExHZjE1YXhKL1B4ZnByVEdML0s0VkIvZU5hblZIaE9CYXo3bmgxV3RvN2hiTFhBK3dpK0lsCjZPcjVqZVFFOUd0OXU1aitIeW9NMmt3RmdjeFZwbjhkSENpNjBwL3hWWExXNEFkcUlRT0JGNnJwRWp2a0RJUFMKUmVLanNLR1JBb0dCQU92Y01YYzNBRjV4aHc5djBHTWUyZW5BOGM5UHhBZTQ3WTdQQjBFb2JBdGlXaEREZk9rNAo5dG03LzZaNVB0aTJRN3pQOWtxUlpyTldpdFFjNU40bTZtY2UrWDhNTG4zRmNLQUdHMWp3Z0duNncyUkgxUm9ZCjEyRnMxaUd4TTd6U2t2SnBOV2lycVU5Sk9PRlFRUjgwR05vejhuRkpZV2gyRGw3c1ZFdExUMmJQQW9HQkFPcDMKcDQ2d3dzM2h3aG11dFNyWmtldGRCNHB1T0ZjMG1DREpQS053Zk5QdDFxVHJ0RTE3Y0NiT01iakRQTytKdUw5awpKQmZwZG1reEFDM3hUMkU3RVp0aEQvT25Oek9qVmQ5a3BiVDl6RHV6V0VHdjd1QndQY0NUeThURmVzMDlyVTBoClZGcW16YURBK0RtNm1jUFFMQkF5RXBoT1REZkxjb1I1K1NPZXIvWDVBb0dBTDV3U0RCdDVJcGRPQ1Fxc0NPWVkKWEx3SzA2c3BTZG5GY2pkT0lwUHpRMVVHRXk0eXo2MGsvd3lZN1ZTNkgrcWl2OEZHMlFTQ3M1NjdoVmVUeDFnWgpwdGsweWJWK3lQcUs0bko1SUxuallnRXhZZE95SzROcUxvdFdxaFJuK2l5VFp3VmZ0NUkzS2Y4QTBWSnU0c3FVClhhOXd0L2QxQnk0VmRvbkQ5akxzZ3pjQ2dZQU1vOGl2bzQzTTVZZStOTEhsam5jVVZoNks4dWdzbzFRMEtFVVIKbG9YVU12VW9UT0NhY0xZYUVYR1N3VXV1cWlFQWlGaDl4WU14cG9lWThuSlNEb29qY3pjVjdvVEdUdDdaUFNiRgp2QXpmaHdxUjkvY0x1R0ZMMld2WnZyK2hBdHN0MWtjaTMrMGo1bU03VVhqcW1uVlZwaTFrY293ZlVlTnBpdDNJCmNzeVBtUUtCZ1FDbnNmbUVkL0l6M04xMG1UZVd1T2RYVmVXS2grcG1BdUtQRzhXUDV6NHIrVWsvL2tWU1R2MEkKaWNsQ0toUHNrTVpKOFNvUmNSb1RTcWY3VlJobzArU0ZVaUQ3b1NMSHIxZUN4ZzM2UTlQRzE0eW1Lb1B5VlJzRAppdklKTGJTbEptRko4bE5zN1RXRnpwWjNoQ2NvRlJlSWNTaTRDWWtLUkNTd1hFSzNKdXFncVE9PQotLS0tLUVORCBSU0EgUFJJVkFURSBLRVktLS0tLQo=
- name: kind-local
  user:
    client-certificate-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSURLVENDQWhHZ0F3SUJBZ0lJSFA3UGUxa0k0WmN3RFFZSktvWklodmNOQVFFTEJRQXdGVEVUTUJFR0ExVUUKQXhNS2EzVmlaWEp1WlhSbGN6QWVGdzB5TkRBMk1UVXhNakU1TWpWYUZ3MHlOVEEyTVRVeE1qSTBNamRhTUR3eApIekFkQmdOVkJBb1RGbXQxWW1WaFpHMDZZMngxYzNSbGNpMWhaRzFwYm5NeEdUQVhCZ05WQkFNVEVHdDFZbVZ5CmJtVjBaWE10WVdSdGFXNHdnZ0VpTUEwR0NTcUdTSWIzRFFFQkFRVUFBNElCRHdBd2dnRUtBb0lCQVFEZDUxQlUKSEdTQ2hLeGo0SEFyaGhINXNjUm1tNFdxZ2ZGQnRkaU55Qzc3NmFFY3I5UXpkYXh2NXpOeklGT0ErRHRZc1Y1NApOdTBNWHNWUmRrbWxxN2JOaTFFS2tPUmpPSHViMVVFZzM3ZHBraUFFSk9iL0VNc2lsalUyOUdzWFJDUzNSUldBCkxyQ2lMYWtMenpiVlpuVlpXS3pXYnJDMGNqV2oxTTUxd1h6SmVVVW52N09oemVxeTBwbWhJKzFoQ3lHU29BTDYKLzVuWlcrZlJHZkprTW1wMHRvYytkYjBoRHh6M1RpWEtpWjJMT240VU5GdTlHZ2lEc1pnWVF0V2dGVmJtN0NETwpFeng4aTJ0Y0UzalBOL2Q3M1hxOWkxVC9kRy81N2U2a0xYWHp2N2N6NHBxazVITTZqK0dMeWhxeWJOR0NqbTFHCjF5aVZ5QzYyeW10RlJjZnpBZ01CQUFHalZqQlVNQTRHQTFVZER3RUIvd1FFQXdJRm9EQVRCZ05WSFNVRUREQUsKQmdnckJnRUZCUWNEQWpBTUJnTlZIUk1CQWY4RUFqQUFNQjhHQTFVZEl3UVlNQmFBRkYvaFlSdG9FV1U3SUJlRQptTVVUazBNVDJIOUVNQTBHQ1NxR1NJYjNEUUVCQ3dVQUE0SUJBUUN1Tkk3ejRBV3d5M2lLL2FoYkdTZ2h6T3JSCk1YditGWHJTNTZuQWluTUVYaUJqaEZneXFSVG1ZcE9FNFBzbUp6N1dYdVAvOUhmQ1hqS1VuSEFIVDBWdDBrTWsKVC9wVjNNWWY0VHRmS0J3bzhQTWlxZEgrUUdMUjhvemtDcE4vS1VmQXViWjZ0NFJjSWdYS3BVM2taKzhqZTE2UQpjd1MwRXFrWXZ0WXRJaFdWREhqZjlOYnl1ZHRNakZkKzl6Uml2VjMwQUFFZnc4cGZ2VkpCQUY3NUsxNm5EY2Z2Ckx6T1BHOGtmc3ZjQmJiNytjY0x0bVBpWEs2R2JzNG11eVljZmtYZWNiS0taNjE0LzdLTE1YWDF6S0ptczNFVW8KUHI4WEJ2aFhzeEc4Q2RJaXJUZE5MN1dtdmFBdElqZ0N6aHZkc3EzZ1h5OTdtdEc0NG5jVHI1Tys5QlhXCi0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K
    client-key-data: LS0tLS1CRUdJTiBSU0EgUFJJVkFURSBLRVktLS0tLQpNSUlFcFFJQkFBS0NBUUVBM2VkUVZCeGtnb1NzWStCd0s0WVIrYkhFWnB1RnFvSHhRYlhZamNndSsrbWhISy9VCk0zV3NiK2N6Y3lCVGdQZzdXTEZlZURidERGN0ZVWFpKcGF1MnpZdFJDcERrWXpoN205VkJJTiszYVpJZ0JDVG0KL3hETElwWTFOdlJyRjBRa3QwVVZnQzZ3b2kycEM4ODIxV1oxV1ZpczFtNnd0SEkxbzlUT2RjRjh5WGxGSjcregpvYzNxc3RLWm9TUHRZUXNoa3FBQyt2K1oyVnZuMFJueVpESnFkTGFIUG5XOUlROGM5MDRseW9tZGl6cCtGRFJiCnZSb0lnN0dZR0VMVm9CVlc1dXdnemhNOGZJdHJYQk40enpmM2U5MTZ2WXRVLzNSditlM3VwQzExODcrM00rS2EKcE9Sek9vL2hpOG9hc216UmdvNXRSdGNvbGNndXRzcHJSVVhIOHdJREFRQUJBb0lCQVFESm80ZTY1cEh1aCtDZQpZVE9NV1NlOFhXeTZVRmdGdUU0aUI3dmdHaWVYZ1pTRkhNRVdnYmRQZUNlb1ZaZUxlZ1Z6Y3JrRlErUGplYnFUCmE0bEFvZWhhbmwzbDNBT3NwWWFzOC90YWcrK0dYdUg0NGcrRmR4MGZNSjdxY085ZkZPeklIRjZOTytBRmZyZzkKb3UyUXZLbWxwbzVueSsyR0NzSHpQVXplZEJPUWZwQ2FQR2VCRHJibHJWdVFib3BLZHd6Z2wxc1RzUW1jWkIwNQpLc09tWjN5ajZySUVIa0Y4VWN6Q2FlV3NYdUJiQ3JSQ3lrTktOeEFlc0Y0aXAyTlY5Rmk5QTFDWW1PT0JuKzFICnNwZC9jZjIvTzRVRXhQYkJxanhEd05ra3pDSmhjRjdkNnQzTUFuMVFyUVVybW5JS2JXa2wvU0tqZVdhNXJnSWMKNis1YnIxa0JBb0dCQVBYYmtCMmNYUnBSeEcrdE05NVJpZmE2cGZDY3YrYUtkcHczZmdoY0hwQ3BVTHJlck5VTwo0V1FYbDB5MHVUc0xSS3JsOStqenljalZUM2NzNklDaEV6UDlOd1owYnFpbmlJWVRWZkl0STRuZ0hqY1JMNGhnCmEwUVoyQ1NlNWhoWk00YUxSWGlkMWUzZ2hTbWFWWlJ4b2VMR05icWUvL3ZjSUFMNVg0S1lZU3l0QW9HQkFPY08KeHl1UGRMTkVKanRMaFRKeGxGTlNobWJybStDbE9ZSi9rMllzd2lCem1rQ01qejZlcnJiL3F4N2V4VEFLa3RwcAp6bCszQ3M0WnJhbTEwVzhCcUdKQThBN1FDcW9BdmFOL1dqWHg5aTFMS21mWnRldXVjRGFMZjNMcnEzcVNFMmtpCmMxVTlRUnBpaHJSQ3dVc1V4cFdEWHBOdFFiMStqZW8yMHJmeU83c2ZBb0dCQU5Lb2NOR09Xdy9rSStaMGg4N2sKR3N4M25SdVBrN1lieWdtTVdzY2E5MjJJUmczNElpcmtkeWRtTjFPWVBtWmkvMUZYZnBYeDNXSGh0QmN2T1lDTgpnNEMyWkdGNWZoK3dmUUEwclIyMm80N05vOVlYT1owbTBJSW5pdFhGK08yLzhMQkZ3UjdhVHFWbURYTmFOQjNmClI1Q2h1UVBRblJIV3lPOERjVnphNTloNUFvR0JBTmVYUkdQeXdQTWIzWWhxR09oT2JoV281TnRYYitTV2hpaXIKblA4ek9CZExobHhBU3RBbEErU2dmaXlacytmMWxielNDTXZxWU55WnZSNmpGYjI4RUQ5TlZEQ2VFYlU2WjdnTQpka0hyZU1ZZVluenYrUHpsa0xKMFN3RVJ3TGpuWDlFelllWGc5OFFFdHFldnVlZXloUEN3MlNnNlE2THFXTVIzClR2cHZ2U2dGQW9HQUhJd2Fzc1JpTzk0VkZmMnFWOW5ZWWpWR3ZjWnp2NG5qTDc5ZXJmTFdMc2JuamlCU1pTL3IKUlEyYThWd095elNZMENQMUFvelRiT2lCeC85bThlaC84UkZxbHFzbFhwTlliYVY2QnRUU3k5MTBDMTZpN1ZjaApTZmVUcmFTdlpVMjY2aFJSbHMzaldjbWcyeFhtRnFwa1JDeE44TzUxNG9QU0lNc3pOcnBpL0dFPQotLS0tLUVORCBSU0EgUFJJVkFURSBLRVktLS0tLQo=
PS C:\Users\butke> cat clusters.yml
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
  - role: control-plane
  - role: worker
  - role: worker
PS C:\Users\butke>
PS C:\Users\butke> kubectl version --client
Client Version: v1.30.0
Kustomize Version: v5.0.4-0.20230601165947-6ce0bf390ce3
PS C:\Users\butke> cd
PS C:\Users\butke> kubectl cluster-info
Kubernetes control plane is running at https://127.0.0.1:52610
CoreDNS is running at https://127.0.0.1:52610/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy

To further debug and diagnose cluster problems, use 'kubectl cluster-info dump'.
PS C:\Users\butke>
                   ku
                   kubectl get nodes
NAME                  STATUS   ROLES           AGE   VERSION
local-control-plane   Ready    control-plane   10d   v1.30.0
local-worker          Ready    <none>          10d   v1.30.0
local-worker2         Ready    <none>          10d   v1.30.0
PS C:\Users\butke> kubectl get nodes -v=8
I0625 23:43:56.180966    5044 loader.go:395] Config loaded from file:  C:\Users\butke\.kube\config
I0625 23:43:56.188011    5044 round_trippers.go:463] GET https://127.0.0.1:52610/api/v1/nodes?limit=500
I0625 23:43:56.188011    5044 round_trippers.go:469] Request Headers:
I0625 23:43:56.188011    5044 round_trippers.go:473]     Accept: application/json;as=Table;v=v1;g=meta.k8s.io,application/json;as=Table;v=v1beta1;g=meta.k8s.io,application/json
I0625 23:43:56.188011    5044 round_trippers.go:473]     User-Agent: kubectl.exe/v1.30.0 (windows/amd64) kubernetes/7c48c2b
I0625 23:43:56.198966    5044 round_trippers.go:574] Response Status: 200 OK in 10 milliseconds
I0625 23:43:56.199494    5044 round_trippers.go:577] Response Headers:
I0625 23:43:56.199494    5044 round_trippers.go:580]     Date: Tue, 25 Jun 2024 18:13:56 GMT
I0625 23:43:56.199494    5044 round_trippers.go:580]     Audit-Id: 3a3f5c26-2001-4773-b96f-ab28111c537b
I0625 23:43:56.199494    5044 round_trippers.go:580]     Cache-Control: no-cache, private
I0625 23:43:56.199494    5044 round_trippers.go:580]     Content-Type: application/json
I0625 23:43:56.199494    5044 round_trippers.go:580]     X-Kubernetes-Pf-Flowschema-Uid: bb399f92-5257-4a44-b759-294207ffa39b
I0625 23:43:56.199494    5044 round_trippers.go:580]     X-Kubernetes-Pf-Prioritylevel-Uid: 166e9f8f-129b-4fc9-bdb9-b5adefa251c7
I0625 23:43:56.200014    5044 request.go:1212] Response Body: {"kind":"Table","apiVersion":"meta.k8s.io/v1","metadata":{"resourceVersion":"9562"},"columnDefinitions":[{"name":"Name","type":"string","format":"name","description":"Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names#names","priority":0},{"name":"Status","type":"string","format":"","description":"The status of the node","priority":0},{"name":"Roles","type":"string","format":"","description":"The roles of the node","priority":0},{"name":"Age","type":"string","format":"","description":"CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is repr [truncated 10193 chars]
NAME                  STATUS   ROLES           AGE   VERSION
local-control-plane   Ready    control-plane   10d   v1.30.0
local-worker          Ready    <none>          10d   v1.30.0
local-worker2         Ready    <none>          10d   v1.30.0
PS C:\Users\butke>
                 > docker run -p 2000:80
"docker run" requires at least 1 argument.
See 'docker run --help'.

Usage:  docker run [OPTIONS] IMAGE [COMMAND] [ARG...]

Create and run a new container from an image
PS C:\Users\butke> docker run -p 2000:80 ngnix
Unable to find image 'ngnix:latest' locally
docker: Error response from daemon: pull access denied for ngnix, repository does not exist or may require 'docker login': denied: requested access to the resource is denied.
See 'docker run --help'.
PS C:\Users\butke> docker pull nginx
Using default tag: latest
latest: Pulling from library/nginx
2cc3ae149d28: Pull complete
1018f2b8dba8: Pull complete
b831e78d8e20: Pull complete
3ab22521e919: Pull complete
5112bf42775b: Pull complete
cbdaf9e4ee2d: Pull complete
a06b6fd631e8: Pull complete
Digest: sha256:9c367186df9a6b18c6735357b8eb7f407347e84aea09beb184961cb83543d46e
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest

What's Next?
  View a summary of image vulnerabilities and recommendations → docker scout quickview nginx
PS C:\Users\butke> docker run -p 2000:80 ngnix
Unable to find image 'ngnix:latest' locally
docker: Error response from daemon: pull access denied for ngnix, repository does not exist or may require 'docker login': denied: requested access to the resource is denied.
See 'docker run --help'.
PS C:\Users\butke> docker run -p 3000:80 ngnix
Unable to find image 'ngnix:latest' locally
docker: Error response from daemon: pull access denied for ngnix, repository does not exist or may require 'docker login': denied: requested access to the resource is denied.
See 'docker run --help'.
PS C:\Users\butke> docker pull nginx
Using default tag: latest
latest: Pulling from library/nginx
Digest: sha256:9c367186df9a6b18c6735357b8eb7f407347e84aea09beb184961cb83543d46e
Status: Image is up to date for nginx:latest
docker.io/library/nginx:latest

What's Next?
  View a summary of image vulnerabilities and recommendations → docker scout quickview nginx
PS C:\Users\butke> docker run -p 3000:80 nginx
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
/docker-entrypoint.sh: Configuration complete; ready for start up
2024/06/25 18:30:24 [notice] 1#1: using the "epoll" event method
2024/06/25 18:30:24 [notice] 1#1: nginx/1.27.0
2024/06/25 18:30:24 [notice] 1#1: built by gcc 12.2.0 (Debian 12.2.0-14)
2024/06/25 18:30:24 [notice] 1#1: OS: Linux 5.15.153.1-microsoft-standard-WSL2
2024/06/25 18:30:24 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2024/06/25 18:30:24 [notice] 1#1: start worker processes
2024/06/25 18:30:24 [notice] 1#1: start worker process 29
2024/06/25 18:30:24 [notice] 1#1: start worker process 30
2024/06/25 18:30:24 [notice] 1#1: start worker process 31
2024/06/25 18:30:24 [notice] 1#1: start worker process 32
2024/06/25 18:30:24 [notice] 1#1: start worker process 33
2024/06/25 18:30:24 [notice] 1#1: start worker process 34
2024/06/25 18:30:24 [notice] 1#1: start worker process 35
2024/06/25 18:30:24 [notice] 1#1: start worker process 36
2024/06/25 18:30:24 [notice] 1#1: start worker process 37
2024/06/25 18:30:24 [notice] 1#1: start worker process 38
2024/06/25 18:30:24 [notice] 1#1: start worker process 39
2024/06/25 18:30:24 [notice] 1#1: start worker process 40
172.17.0.1 - - [25/Jun/2024:18:30:53 +0000] "GET / HTTP/1.1" 200 615 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/126.0.0.0 Safari/537.36" "-"
2024/06/25 18:30:53 [error] 30#30: *1 open() "/usr/share/nginx/html/favicon.ico" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /favicon.ico HTTP/1.1", host: "localhost:3000", referrer: "http://localhost:3000/"
172.17.0.1 - - [25/Jun/2024:18:30:53 +0000] "GET /favicon.ico HTTP/1.1" 404 555 "http://localhost:3000/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/126.0.0.0 Safari/537.36" "-"
2024/06/25 18:37:06 [notice] 1#1: signal 2 (SIGINT) received, exiting
2024/06/25 18:37:06 [notice] 29#29: exiting
2024/06/25 18:37:06 [notice] 30#30: exiting
2024/06/25 18:37:06 [notice] 32#32: exiting
2024/06/25 18:37:06 [notice] 33#33: exiting
2024/06/25 18:37:06 [notice] 31#31: exiting
2024/06/25 18:37:06 [notice] 35#35: exiting
2024/06/25 18:37:06 [notice] 36#36: exiting
2024/06/25 18:37:06 [notice] 40#40: exiting
2024/06/25 18:37:06 [notice] 37#37: exiting
2024/06/25 18:37:06 [notice] 34#34: exiting
2024/06/25 18:37:06 [notice] 38#38: exiting
2024/06/25 18:37:06 [notice] 39#39: exiting
2024/06/25 18:37:06 [notice] 35#35: exit
2024/06/25 18:37:06 [notice] 33#33: exit
2024/06/25 18:37:06 [notice] 36#36: exit
2024/06/25 18:37:06 [notice] 32#32: exit
2024/06/25 18:37:06 [notice] 29#29: exit
2024/06/25 18:37:06 [notice] 31#31: exit
2024/06/25 18:37:06 [notice] 34#34: exit
2024/06/25 18:37:06 [notice] 30#30: exit
2024/06/25 18:37:06 [notice] 40#40: exit
2024/06/25 18:37:06 [notice] 37#37: exit
2024/06/25 18:37:06 [notice] 38#38: exit
2024/06/25 18:37:06 [notice] 39#39: exit
2024/06/25 18:37:06 [notice] 1#1: signal 14 (SIGALRM) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 32
2024/06/25 18:37:06 [notice] 1#1: worker process 32 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: worker process 34 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: signal 29 (SIGIO) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 37
2024/06/25 18:37:06 [notice] 1#1: worker process 37 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: signal 29 (SIGIO) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 38
2024/06/25 18:37:06 [notice] 1#1: worker process 38 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: signal 29 (SIGIO) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 35
2024/06/25 18:37:06 [notice] 1#1: worker process 35 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: worker process 39 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: signal 29 (SIGIO) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 29
2024/06/25 18:37:06 [notice] 1#1: worker process 29 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: signal 29 (SIGIO) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 36
2024/06/25 18:37:06 [notice] 1#1: worker process 36 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: signal 29 (SIGIO) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 31
2024/06/25 18:37:06 [notice] 1#1: worker process 31 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: signal 29 (SIGIO) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 30
2024/06/25 18:37:06 [notice] 1#1: worker process 30 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: signal 29 (SIGIO) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 33
2024/06/25 18:37:06 [notice] 1#1: worker process 33 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: signal 29 (SIGIO) received
2024/06/25 18:37:06 [notice] 1#1: signal 17 (SIGCHLD) received from 40
2024/06/25 18:37:06 [notice] 1#1: worker process 40 exited with code 0
2024/06/25 18:37:06 [notice] 1#1: exit
PS C:\Users\butke> kubectl run ngix-test --image= ngnix -port= 80
error: unknown shorthand flag: 'p' in -port=
See 'kubectl run --help' for usage.
PS C:\Users\butke> kubectl run ngix-test --image= ngnix -port= 80
error: unknown shorthand flag: 'p' in -port=
See 'kubectl run --help' for usage.
PS C:\Users\butke> kubectl run ngix-test --image=ngnix -port=80
error: unknown shorthand flag: 'p' in -port=80
See 'kubectl run --help' for usage.
PS C:\Users\butke> kubectl run nginx --image=nginx --port=80
pod/nginx created
PS C:\Users\butke> kubectl get nodes
NAME                  STATUS   ROLES           AGE   VERSION
local-control-plane   Ready    control-plane   10d   v1.30.0
local-worker          Ready    <none>          10d   v1.30.0
local-worker2         Ready    <none>          10d   v1.30.0
PS C:\Users\butke> kubectl get pods
NAME    READY   STATUS    RESTARTS   AGE
nginx   1/1     Running   0          89s
PS C:\Users\butke> kubectl logs nginx-test
error: error from server (NotFound): pods "nginx-test" not found in namespace "default"
PS C:\Users\butke> kubectl logs nginx
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
/docker-entrypoint.sh: Configuration complete; ready for start up
2024/06/25 18:39:30 [notice] 1#1: using the "epoll" event method
2024/06/25 18:39:30 [notice] 1#1: nginx/1.27.0
2024/06/25 18:39:30 [notice] 1#1: built by gcc 12.2.0 (Debian 12.2.0-14)
2024/06/25 18:39:30 [notice] 1#1: OS: Linux 5.15.153.1-microsoft-standard-WSL2
2024/06/25 18:39:30 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2024/06/25 18:39:30 [notice] 1#1: start worker processes
2024/06/25 18:39:30 [notice] 1#1: start worker process 32
2024/06/25 18:39:30 [notice] 1#1: start worker process 33
2024/06/25 18:39:30 [notice] 1#1: start worker process 34
2024/06/25 18:39:30 [notice] 1#1: start worker process 35
2024/06/25 18:39:30 [notice] 1#1: start worker process 36
2024/06/25 18:39:30 [notice] 1#1: start worker process 37
2024/06/25 18:39:30 [notice] 1#1: start worker process 38
2024/06/25 18:39:30 [notice] 1#1: start worker process 39
2024/06/25 18:39:30 [notice] 1#1: start worker process 40
2024/06/25 18:39:30 [notice] 1#1: start worker process 41
2024/06/25 18:39:30 [notice] 1#1: start worker process 42
2024/06/25 18:39:30 [notice] 1#1: start worker process 43
PS C:\Users\butke> kubectl logs nginx
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
/docker-entrypoint.sh: Configuration complete; ready for start up
2024/06/25 18:39:30 [notice] 1#1: using the "epoll" event method
2024/06/25 18:39:30 [notice] 1#1: nginx/1.27.0
2024/06/25 18:39:30 [notice] 1#1: built by gcc 12.2.0 (Debian 12.2.0-14)
2024/06/25 18:39:30 [notice] 1#1: OS: Linux 5.15.153.1-microsoft-standard-WSL2
2024/06/25 18:39:30 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2024/06/25 18:39:30 [notice] 1#1: start worker processes
2024/06/25 18:39:30 [notice] 1#1: start worker process 32
2024/06/25 18:39:30 [notice] 1#1: start worker process 33
2024/06/25 18:39:30 [notice] 1#1: start worker process 34
2024/06/25 18:39:30 [notice] 1#1: start worker process 35
2024/06/25 18:39:30 [notice] 1#1: start worker process 36
2024/06/25 18:39:30 [notice] 1#1: start worker process 37
2024/06/25 18:39:30 [notice] 1#1: start worker process 38
2024/06/25 18:39:30 [notice] 1#1: start worker process 39
2024/06/25 18:39:30 [notice] 1#1: start worker process 40
2024/06/25 18:39:30 [notice] 1#1: start worker process 41
2024/06/25 18:39:30 [notice] 1#1: start worker process 42
2024/06/25 18:39:30 [notice] 1#1: start worker process 43
PS C:\Users\butke>
                   kubectl run postgres --image=postgres -port=80
error: unknown shorthand flag: 'p' in -port=80
See 'kubectl run --help' for usage.
PS C:\Users\butke> docker pull postgres
Using default tag: latest
latest: Pulling from library/postgres
2cc3ae149d28: Already exists
d1a63825d58e: Pull complete
ed6f372fe58d: Pull complete
35f975e69306: Pull complete
40c4fe86e99d: Pull complete
4795e1a32ff6: Pull complete
bcb5a54ae87d: Pull complete
d3983228bec6: Pull complete
5378bf7229e9: Pull complete
bba3241011a6: Pull complete
5e1d0413d05a: Pull complete
6a489170d05e: Pull complete
440b39aff272: Pull complete
582c79113570: Pull complete
Digest: sha256:46aa2ee5d664b275f05d1a963b30fff60fb422b4b594d509765c42db46d48881
Status: Downloaded newer image for postgres:latest
docker.io/library/postgres:latest

What's Next?
  View a summary of image vulnerabilities and recommendations → docker scout quickview postgres
PS C:\Users\butke> kubectl run postgres --image=postgres --port=80
pod/postgres created
PS C:\Users\butke> kubectl get pods
NAME       READY   STATUS              RESTARTS   AGE
nginx      1/1     Running             0          9m35s
postgres   0/1     ContainerCreating   0          9s
PS C:\Users\butke>