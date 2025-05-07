# Python-files
Código(s) de Python
import numpy as np

while True:
    try:
        D=int(input('Olá sou o Programa de Aplicação das Áreas das Principais Figuras Geométricas(P.A.Á.P.F.G.); '
            '\nDIGITE [ 1 ] para saber a área de um quadrado; '
            '\nDIGITE [ 2 ] para saber a área de um retângulo/paralelogramo; '
            '\nDIGITE [ 3 ] para saber a área do triângulo; '
            '\nDIGITE [ 4 ] para saber a área do triângulo equilátero; '
            '\nDIGITE [ 5 ] para saber a área do Herão; '
            '\nDIGITE [ 6 ] para saber a área do trapézio; '
            '\nDIGITE [ 7 ] para saber a área do losango; '
            '\nDIGITE [ 8 ] para saber a área do círculo/circunferência; '
            '\n____________________Figuras Espacias em 3 dimensões____________________'
            '\nDIGITE [ 9 ] para saber a área cubo´/volume; '
            '\nDIGITE [ 10 ] para saber a paralelepípedo/volume; '
            '\nDIGITE [ 11 ] para saber a Prisma/área lateral/volume; '
            '\nDIGITE [ 12 ] para saber a área da pirâmide/ área total/ volume; '
            '\nDIGITE [ 13 ] para saber a área do cilindro/área lateral/volume; '
            '\nDIGITE [ 14 ] para saber a área do cone/ área lateral/ volume; '
            '\nDIGITE [ 15 ] a área da esfera/ volume;'
            '\nDIGITE [ 16 ] para sair do programa.'
            '\n\n'))
    except ValueError:
        print('Erro: Digite um número inteiro válido.')
        continue
    if D==1:
        L=float(input('Diga-me o valor do lado do quadrado.'))
        re=L**2
        print('Este é o resultado:{:.2f}'.format(re))

    elif D==2:
        b=float(input('Pode-me dizer o valor da base do retângulo/paralelogramo?'))
        h=float(input('Pode-me dizer o valor da altura do retângulo/paralelogramo?'))
        re=b*h
        print('Este é o resultado:{:.2f}'.format(re))

    elif D==3:
        b = float(input('Pode-me dizer o valor da base do triângulo?'))
        h = float(input('Pode-me dizer o valor da altura do triângulo?'))
        re = (b * h)/2
        print('Este é o resultado:{:.2f}'.format(re))

    elif D==4:
            L = float(input('Diga-me o valor do lado do triângulo equilátero.'))
            re=((L**2)*3**0.5)/4
            print('Este é o resultado:{:.2f}'.format(re))

    elif D==5:
            a = float(input('Diga-me o valor do lado do herão.'))
            b = float(input('Diga-me o valor do segundo lado do herão.'))
            c = float(input('Diga-me o valor do terceiro lado do herão.'))
            S= (a+b+c)/2
            re=(S*(S-a)*(S-b)*(S-c))**0.5
            print('Este é o resultado:{:.2f}'.format(re))

    elif D==6:
                B=float(input('Diga-me o valor da base maior.'))
                b=float(input('Diga-me o valor da base menor.'))
                h=float(input('Pode-me dizer o valor da altura do trapézio?'))
                re=((B+b)*h)/2
                print('Este é o resultado:{:.2f}'.format(re))

    elif D==7:
                s=float(input('Diga-me o valor da diagonal maior?'))
                d=float(input('Diga-me o valor da diagonal menor?'))
                re=(s*d)/2
                print('Este é o resultado:{:.2f}'.format(re))

    elif D==8:
                Q=float(input('Digite [ 1 ] para saber a área do círculo, caso contrário você descubrirá a circunferência. '))

                if Q==1:
                    R=float(input('Diga-me o valor do raio.'))
                    re=np.pi*R**2
                    print('Este é o resultado:{:.2f}'.format(re))

                else:
                    R=float(input('Diga-me o valor do raio.'))
                    re=2*np.pi*R
                    print('Este é o resultado:{:.2f}'.format(re))

    elif D==9:
                    Q = float(input('Digite [ 1 ] para saber a área do cubo, caso contrário você descobrirá o valor do volume. '))
                    if Q==1:
                            L = float(input('Diga-me o valor do lado do cubo.'))
                            re=6*L**2
                            print('Este é o resultado:{:.2f}'.format(re))

                    else:
                        L = float(input('Diga-me o valor do lado do cubo.'))
                        re=L**3
                        print('Este é o resultado:{:.2f}'.format(re))

    elif D==10:
                    Q=float(input('Digite [ 1 ] para saber a área total de um paralelepípedo; \ncaso contrário você descobrirá o valor do volume.'))
                    if Q==1:
                        a=float(input('Diga-me o valor do lado do paralelepípedo.'))
                        b=float(input('Diga-me o valor do segundo lado do paralelepípedo.'))
                        c=float(input('Diga-me o valor do terceiro lado do paralelepípedo.'))
                        re= 2*(a*b+a*c+b*c)
                        print('Este é o resultado:{:.2f}'.format(re))
                    else:
                        a = float(input('Diga-me o valor do lado do paralelepípedo.'))
                        b = float(input('Diga-me o valor do segundo lado do paralelepípedo.'))
                        c = float(input('Diga-me o valor do terceiro lado do paralelepípedo.'))
                        re=a*b*c
                        print('Este é o resultado:{:.2f}'.format(re))

    elif D==11:
                Q=float(input('Digite [ 1 ] para saber a área lateral; \ndigite [ 2 ] para saber o valor da área total e \ndigite [ 3 ] para saber o valor do volume.'))
                if Q==1:
                    P=float(input('Diga-me o valor do perímetro.'))
                    h=float(input('Diga-me o valor da altura.'))
                    re=P*h
                    print('Este é o resultado:{:.2f}'.format(re))

                elif Q==2:
                    Al=float(input('Diga-me o valor da área lateral.'))
                    Ab= float(input('Diga-me o valor da base.'))
                    re=Al + 2*Ab
                    print('Este é o resultado:{:.2f}'.format(re))

                elif Q==3:
                    Ab = float(input('Diga-me o valor da base.'))
                    h = float(input('Diga-me o valor da altura.'))
                    re=Ab*h
                    print('Este é o resultado:{:.2f}'.format(re))

    elif D==12:
                    Q = float(input('Digite [ 1 ] para saber a área lateral; \ndigite [ 2 ] para saber o valor da área total e \ndigite [ 3 ] para saber o valor do volume.'))
                    if Q==1:
                        P = float(input('Diga-me o valor do perímetro da base.'))
                        a = float(input('Diga-me o valor da apótema'))
                        re=(P*a)/2
                        print('Este é o resultado:{:.2f}'.format(re))

                    elif Q==2:
                        Al = float(input('Diga-me o valor da área lateral.'))
                        Ab = float(input('Diga-me o valor da base.'))
                        re= Al + Ab
                        print('Este é o resultado:{:.2f}'.format(re))

                    elif Q==3:
                        Ab = float(input('Diga-me o valor da base.'))
                        h = float(input('Diga-me o valor da altura.'))
                        re=(Ab*h)/3
                        print('Este é o resultado:{:.2f}'.format(re))
    elif D==13:
                    Q = float(input('Digite [ 1 ] para saber a área lateral; \ndigite [ 2 ] para saber o valor da área total e \ndigite [ 3 ] para saber o valor do volume.'))
                    if Q==1:
                        R = float(input('Diga-me o valor do raio.'))
                        h = float(input('Diga-me o valor da altura.'))
                        re=2*np.pi*R*h
                        print('Este é o resultado:{:.2f}'.format(re))

                    elif Q==2:
                        R = float(input('Diga-me o valor do raio.'))
                        h = float(input('Diga-me o valor da altura.'))
                        re=2*np.pi*R*(R+h)
                        print('Este é o resultado:{:.2f}'.format(re))

                    elif Q==3:
                        R = float(input('Diga-me o valor do raio.'))
                        h = float(input('Diga-me o valor da altura.'))
                        re=np.pi*(R**2)*h
                        print('Este é o resultado:{:.2f}'.format(re))

    elif D==14:
                Q = float(input('Digite [ 1 ] para saber a área lateral; \ndigite [ 2 ] para saber o valor da área total e \ndigite [ 3 ] para saber o valor do volume.'))
                if Q==1:
                    R = float(input('Diga-me o valor  do raio.'))
                    G = float(input('Diga-me o valor da geratriz.'))
                    re=np.pi*R*G
                    print('Este é o resultado:{:.2f}'.format(re))
                elif Q==2:
                    R = float(input('Diga-me o valor do raio.'))
                    G = float(input('Diga-me o valor da geratriz.'))
                    re=np.pi*R*(R + G)
                    print('Este é o resultado:{:.2f}'.format(re))

                elif Q==3:
                    R = float(input('Diga-me o valor raio.'))
                    h = float(input('Diga-me o valor da altura.'))
                    re=(np.pi*(R**2)*h)/3
                    print('Este é o resultado:{:.2f}'.format(re))

    elif D==15:
                    Q = float(input('Digite [ 1 ] para saber a área total de um paralelepípedo; \ncaso contrário você descobrirá o valor do volume.'))
                    if Q==1:
                        R = float(input('Diga-me o valor de do raio.'))
                        re=4*np.pi*R**2
                        print('Este é o resulatado:{:.2f}'.format(re))

                    else:
                        R = float(input('Diga-me o valor do raio.'))
                        re=(4/3)*np.pi*R**3
                        print('Este é o resultado:{:.2f}'.format(re))

    elif D==16:
        print('O programa foi encerrado.')

    elif D>17:
        print('Número inválido. Tente novamente.')
        break
