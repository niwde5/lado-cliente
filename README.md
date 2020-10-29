#Actividad T3_03

#####Avanze del proyecto con formularios dinámicos de login y registro, para su proyecto, que dispongan de elementos generados y validados con lenguaje del lado del cliente, mediante un Framework seleccionado a criterio propio.
'''html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/bootstrap.min.css">
    <link rel="stylesheet" href="css/estilos.css">
    <link rel="stylesheet" href="css/styles.css">
    <title>Document</title>
    <script src="js/jquery-3.5.1.min.js"></script>
    <script src="js/bootstrap.min.js"></script>    
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <script src="js/valida.js"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->    
   <script src="https://cdn.jsdelivr.net/npm/jquery-validation@1.19.0/dist/jquery.validate.js"></script>
</head>
<body>
    <nav class='navbar navbar-expand-md navbar-light bg-warning h6'>
        <div class="container font-weight-bold">
            <a href="#" class='navbar-brand'>SalonDeEventos</a>
            <button class="navbar-toggler" data-toggle="collapse" data-target="#first-navbar">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div id="first-navbar" class="collapse navbar-collapse">
                <ul class="navbar-nav ml-auto">
                    <li class="nav-item"><a class="nav-link" href="#">Principal</a></li>
                    <li class="nav-item"><a class="nav-link" href="#consultas">Consultar</a></li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" data-toggle="modal" data-target="#contacto">
                            Contacto
                        </a>
                    </li>                    
                    <li class="nav-item">
                        <a id="inits" class="nav-link btn btn-success btn-sm text-light" href="#" data-toggle="modal" data-target="#login">Iniciar Sesión                            
                        </a>
                    </li>
                    <li id="boton-r" class="nav-item ml-2">
                        <a class="nav-link btn btn-primary btn-sm text-light" href="#" data-toggle="modal" data-target="#registro">Registrarse
                        </a>
                    </li>
                </ul>                
            </div>
        </div>
    </nav>    
    <section class="home" id="home">
        <div id="reg-exitoso" class="alert alert-success alert-dismissible text-center">
            <button type="button" class="close" data-dismiss="alert">
                <span>×</span>
            </button>
             Registro <strong>Exitoso</strong> 
        </div>
        <div class="max-width">
            <div class="home-content">
                <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
                    <div class="carousel-inner">
                      <div class="carousel-item active">
                        <img src="img/ev1.jpg" class="d-block w-100" width="800" height="550" alt="...">
                        <div class="carousel-caption d-none d-md-block">
                            <h5>Servicios de arreglos florales</h5>                    
                        </div>
                      </div>
                      <div class="carousel-item">
                        <img src="img/ev2.png" class="d-block w-100" width="800" height="550" alt="...">
                        <div class="carousel-caption d-none d-md-block">
                            <h5>Servicios de mesebrios</h5>                    
                        </div>
                      </div>
                      <div class="carousel-item">
                        <img src="img/ev3.jpg" class="d-block w-100" width="800" height="550" alt="...">
                        <div class="carousel-caption d-none d-md-block">
                            <h5>Servicios de de luz y sonido</h5>                    
                        </div>
                      </div>
                      <div class="carousel-item">
                        <img src="img/ev4.jpg" class="d-block w-100" width="800" height="550" alt="...">
                        <div class="carousel-caption d-none d-md-block">
                            <h5>Servicios de de luz y sonido</h5>                    
                        </div>
                      </div>
                      <div class="carousel-item">
                        <img src="img/ev5.jpg" class="d-block w-100" width="800" height="550" alt="...">
                        <div class="carousel-caption d-none d-md-block">
                            <h5>Servicios de de luz y sonido</h5>                    
                        </div>
                      </div>
                      </div>
                      <div class="carousel-item">
                        <img src="img/ev7.jpg" class="d-block w-100" width="800" height="550" alt="...">
                        <div class="carousel-caption d-none d-md-block">
                            <h5>Servicios de de luz y sonido</h5>                    
                        </div>
                      </div>
                      <div class="carousel-item">
                        <img src="img/ev8.jpg" class="d-block w-100" width="800" height="550" alt="...">
                        <div class="carousel-caption d-none d-md-block">
                            <h5>Servicios de de luz y sonido</h5>                    
                        </div>
                      </div>
                    </div>
                    <a class="carousel-control-prev ml-1" href="#carouselExampleControls" role="button" data-slide="prev">
                      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                      <span class="sr-only">Previous</span>
                    </a>
                    <a class="carousel-control-next mr-2" href="#carouselExampleControls" role="button" data-slide="next">
                      <span class="carousel-control-next-icon" aria-hidden="true"></span>
                      <span class="sr-only">Next</span>
                    </a>
                  </div>
            </div>
        </div>
    </section>

    <section class="about" id="consultas">
        <div class="max-width">
            <h2 class="title">Consulta los días disponibles</h2>
            <div class="about-content">                    
                <div class="column">
                    <div class="text">Tenemos una fecha especial para tí y tus invitados <span class="typing-2"></span></div>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi ut voluptatum eveniet doloremque autem excepturi eaque, sit laboriosam voluptatem nisi delectus. Facere explicabo hic minus accusamus alias fuga nihil dolorum quae. Explicabo illo unde, odio consequatur ipsam possimus veritatis, placeat, ab molestiae velit inventore exercitationem consequuntur blanditiis omnis beatae. Dolor iste excepturi ratione soluta quas culpa voluptatum repudiandae harum non.</p>
                    <br>
                    <div class="calendar">
                        <div class="calendar__info">
                            <div class="calendar__prev" id="prev-month">&#9664;</div>
                            <div class="calendar__month" id="month"></div>
                            <div class="calendar__year" id="year"></div>
                            <div class="calendar__next" id="next-month">&#9654;</div>
                        </div>
                    
                        <div class="calendar__week">
                            <div class="calendar__day calendar__item">Mon</div>
                            <div class="calendar__day calendar__item">Tue</div>
                            <div class="calendar__day calendar__item">Wed</div>
                            <div class="calendar__day calendar__item">Thu</div>
                            <div class="calendar__day calendar__item">Fri</div>
                            <div class="calendar__day calendar__item">Sat</div>
                            <div class="calendar__day calendar__item">Sun</div>
                        </div>
                        <div class="calendar__dates" id="dates"></div>
                    </div>                          
                </div>
            </div>
        </div>
    </section>    
    <footer>
        <span>Creado por <a href="#">ISC-TECNM-7MO-EQUIPO N</a> | <span class=>&copy;</span> 2020 Todos los derechos reservados.</span>
    </footer>
    <!--modals iniciar sesión-->
    <div class="modal fade" id="login" tabindex="-1" role="dialog" arialabelledby=" myModalLabel" aria-hidden="true">
        <div class="modal-dialog" rol="document">
            <div class="modal-content bg-transparent text-light font-weight-bold">
                <div class="modal-body">
                    <form class="form-container">
                        <button id="closes" type="button" class="close text-light" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                        </button>
                        <div class="form-group">
                            <h3>Iniciar Sesión</h3>
                            <label for="exampleInputEmail1">Correo Electrónico</label>
                            <input type="email" class="form-control" id="init-correo"
                                aria-describedby="emailHelp">
                        </div>
                        <div class="form-group">
                            <label for="exampleInputPassword1">Contraseña</label>
                            <input type="password" class="form-control" id="init-pass">
                        </div>
                        <div class="form-group form-check">
                            <input type="checkbox" class="form-check-input" id="exampleCheck1">
                            <label class="form-check-label" for="exampleCheck1">Recordarme</label>
                        </div>
                        <button id="iniciar" type="button" class="btn btn-success btn-block">
                            <i class="fa fa-user mr-1"></i>Iniciar Sesión</button>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!--modal formulario de registro-->
    <div class="modal fade" id="registro" tabindex="-1" role="dialog" arialabelledby=" myModalLabel"
        aria-hidden="true">
        <div class="modal-dialog" rol="document">
            <div class="modal-content bg-transparent text-light font-weight-bold">
                <div class="modal-body">
                    <form class="form-container needs-validation">
                        <button id="closer" type="button" class="close text-light" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                        </button>
                        <div class="form-group">
                            <h3>Datos de registro</h3>
                                <input class="form-control" placeholder="Nombre" type="text" id="nombre" name="nombre" required>       
                                <span id="a1" class="alertas">Campo requerido</span>
                        </div>
                        <div class="form-group">
                            <input placeholder="Correo Electrónico" type="email" class="form-control has danger" id="email-registro" name="email">
                            <span id="a2" class="alertas">Campo requerido</span>
                        </div>
                        <div class="form-group">
                            <input placeholder="Teléfono" type="tel" class="form-control" id="tel-number" name="tel">
                            <span id="a3" class="alertas">Campo requerido</span>
                        </div>
                        <div class="form-group">
                            <input placeholder="Contraseña" type="password" class="form-control" id="pwd-1" name="pwd1">
                            <span id="a4" class="alertas">Campo requerido</span>
                        </div>
                        <div class="form-group">
                            <input placeholder="Confirmar Contraseña" type="password" class="form-control"
                                id="pwd-2" name="pwd2">
                            <span id="a5" class="alertas">Campo requerido</span>
                        </div>
                        <button id="register" type="button" class="btn btn-primary btn-block">
                            <i class="fa fa-user mr-1"></i>Registrarme</button>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!--modals contactanos-->
    <div class="modal fade" id="contacto" tabindex="-1" role="dialog" arialabelledby=" myModalLabel" aria-hidden="true">
        <div class="modal-dialog" rol="document">
            <div class="modal-content bg-transparent text-light font-weight-bold">
                <div class="modal-body">
                    <form class="form-container">
                        <button type="button" class="close text-light" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                        </button>
                        <h3>Contáctanos</h3>
                        <div class="form-group">
                            <div class="form-group">
                                <input class="form-control" type="text" placeholder="Name" required>
                            </div>
                            <div class="form-group">
                                <input class="form-control" type="email" placeholder="Email" required>
                            </div>
                        </div>
                        <div class="form-group">
                            <input class="form-control" type="text" placeholder="Subject" required>
                        </div>
                        <div class="form-group">
                            <textarea class="form-control" cols="30" rows="5" placeholder="Message.."
                                required></textarea>
                        </div>
                        <button type="submit" class="btn btn-success btn-block">
                            <i class="fa fa-user mr-1"></i>Enviar</button>
                    </form>
                </div>
            </div>
        </div>
        <script src="js/calendar.js"></script>
</body>
</html>
'''
##pantalla principal
![imagen](https://user-images.githubusercontent.com/72904875/97513144-0dd46200-1951-11eb-818f-b52fe1ceb982.png)

##inicio de sesion
![imagen](https://user-images.githubusercontent.com/72904875/97513172-204e9b80-1951-11eb-8754-70d6a3754258.png)

##formulario
![imagen](https://user-images.githubusercontent.com/72904875/97513195-38beb600-1951-11eb-940d-3107f3694b5e.png)
